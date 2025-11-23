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

## Troubleshooting
* **Pop-up Blockers:** If the download does not start immediately, check your address bar for a "Pop-up blocked" icon and allow it.
* **400 Bad Request:** If you see network errors, ensure you are using the version of the script that requests the standard `itemArray` rather than extended fields (like specific department IDs) which are restricted by the Costco API.
