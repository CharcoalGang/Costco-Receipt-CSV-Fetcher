# Costco Receipt Downloader

A JavaScript snippet that fetches your Costco order history and converts it into a detailed CSV format suitable for spreadsheets (Excel, Google Sheets).

## Features
* **Detailed Data:** Exports 28 columns including Item Name, Unit Price, Quantity, Tax Flags, and Discounts.
* **Smart Math:** Automatically calculates individual unit prices (e.g., price per steak) and handles item quantities.
* **Adjustments:** Properly handles "Instant Savings," CRV taxes, and other surcharges by attaching them to the correct items rather than listing them as separate rows.
* **No Extension Required:** Runs directly in your browser console.

## How to Use

1. **Login:** Go to [www.costco.com](https://www.costco.com) and log in to your account.
2. **Navigate:** Go to the [Order Status page](https://www.costco.com/OrderStatusCmd).
   * *Note:* You must be on this specific page for the script to access the correct authorization tokens.
3. **Open Console:**
   * **Windows:** Press `F12` or right-click anywhere on the page and select **Inspect**, then click the **Console** tab.
   * **Mac:** Press `Command + Option + J` (Chrome) or `Command + Option + C` (Safari).
4. **Run:** Copy the entire script, paste it into the console, and press **Enter**.
5. **Download:** The script will fetch your history and automatically trigger a `.csv` download.

## Configuration

### Changing the Date Range
By default, the script pulls receipts starting from **January 1, 2023**. To change this:

1. Scroll to the bottom of the script to the `downloadFullCsv` function.
2. Find the line: `var startDateStr = '01/01/2023';`
3. Update the date using the `MM/DD/YYYY` format.

## Credits & Attribution
This script is a mix of existing tools and AI generation. I am not a programmer, but I used **Google Gemini** to merge different codebases into this working solution.

* **Original Logic:** The fetching logic is based on the work by [Ankur Dave](https://github.com/ankurdave/beancount_import_sources/blob/main/download/download_costco_receipts.js).
* **Code Refinement:** Updated and merged with detailed CSV processing logic using Gemini.

## Disclaimer & Maintenance
**Please Note:** I have no programming knowledge. This repository was created simply to share a solution that worked for me at the time.

* **This project will not be actively maintained.**
* If Costco changes their website structure or API, this script may stop working.
* I cannot provide technical support, bug fixes, or feature updates.
