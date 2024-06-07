+++
title = 'Uonwifi'
date = 2024-06-03T13:08:07Z
draft = true
+++

After a lot of trial and error I was able to finish it.

```
//make sure to install puppeteer 
const puppeteer = require('puppeteer');
const fs = require('fs');

async function uonwifi(username, password) {
  const browser = await puppeteer.launch({ headless: true, ignoreHTTPSErrors: true });
  const page = await browser.newPage();

  try {
    const response = await page.goto('https://gstatic.com/generate_204', { waitUntil: 'networkidle2' });

    // Check if the response indicates that you're already logged in
    if (response.status() === 200) {
      console.log('Already logged in!');
      await browser.close();
      return;
    }

    await page.type('#ft_un', username);
    await page.type('#ft_pd', password);
    await page.click('body > div > div > form > div:nth-child(8) > input[type=submit]');
    
    const screenshotsDir = './screenshots';
    if (!fs.existsSync(screenshotsDir)) {
      fs.mkdirSync(screenshotsDir);
    }
    
    const screenshotPath = `${screenshotsDir}/loggedin.png`;
    await page.screenshot({ path: screenshotPath });
    
    console.log(`Screenshot saved to ${screenshotPath}`);
  } catch (error) {
    if (error.toString().includes('net::ERR_ABORTED')) {
      console.log('Already logged in!');
    } else {
      console.error('Error navigating to the page:', error);
    }
  } finally {
    await browser.close();
  }
}

const command = process.argv[2];
const username = process.argv[3];
const password = process.argv[4];

if (command === 'uonwifi' && username && password) {
  uonwifi(username, password);
} else {
  console.log('Wrong argument or missing username/password!');
}
``
