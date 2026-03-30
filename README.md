E-Commerce Order & Invoice Automation (n8n)
This project is a fully automated E-Commerce Order Management System built using n8n. It handles everything from the moment a customer places an order to the final delivery of a professional PDF invoice, ensuring zero manual data entry and real-time inventory management.

🚀 Features
Real-time Order Capture: Uses Webhooks to trigger the workflow instantly when a new order is placed.

Database Integration: Automatically appends order details to Google Sheets for centralized record-keeping.

Multi-Channel Notifications: * Sends an instant order confirmation email to the Customer via Gmail.

Sends a real-time order alert to the Admin/Team via Slack.

Automated Inventory Management: Reads current stock levels from Google Sheets and updates them automatically based on the order quantity.

Dynamic Document Generation: Transforms order data into a formatted HTML-to-PDF Invoice.

Automated Billing: Automatically emails the generated PDF invoice to the customer upon successful stock update.

🛠️ Tech Stack
Automation Tool: n8n

Database: Google Sheets

Communication: Gmail API, Slack API

Tools: Webhooks, HTML-to-PDF Converter, Edit Fields (Data Transformation)

📦 Workflow Logic (Step-by-Step)
Webhook: Listens for incoming POST requests containing order details.

Append to Sheet: Saves the raw order data into a Google Sheet.

Slack Notification: Posts a message to a specific channel to alert the fulfillment team.

Order Confirmation: Sends a "Thank You" email to the customer.

Get/Update Stock: Checks if the item is in stock and decrements the quantity in the inventory sheet.

Edit Fields: Maps and formats the data (Price, Name, Date) for the invoice.

HTML to PDF: Generates a professional invoice using a custom HTML template.

Send Invoice: Emails the final PDF attachment to the customer's email address.

🖼️ Workflow Screenshot
<img width="1287" height="496" alt="image" src="https://github.com/user-attachments/assets/99fc156d-09ec-4ebc-9ec8-02156c79ba2a" />


⚙️ How to Use
Import Workflow: Download the .json file from this repository and import it into your n8n instance.

Configure Credentials:

Set up Google Sheets API credentials.

Connect your Gmail and Slack accounts.

Webhook Setup: Point your e-commerce store (or Postman) to the Webhook URL provided by n8n.

Templates: Customize the HTML code in the "Convert HTML to PDF" node to match your brand's invoice style.

