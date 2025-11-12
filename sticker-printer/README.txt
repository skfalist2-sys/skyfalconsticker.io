STICKER PRINTER SETUP
=====================

1. UPLOAD TO NETLIFY:
   - Go to https://app.netlify.com/drop
   - Drag the entire "sticker-printer" folder
   - Wait for deployment
   - Copy your site URL (e.g., https://amazing-site-123.netlify.app)

2. APPSHEET SETUP:
   Use this URL format in your Open Website action:

   =CONCATENATE(
     "https://yoursite.netlify.app/print.html?",
     "sku=", ENCODEURL([SKU]),
     "&title=", ENCODEURL(IF(LEN([Title]) > 60, LEFT([Title], 60) & "…", [Title])),
     "&condition=", ENCODEURL([Condition]),
     "&detail=", ENCODEURL([Detail])
   )

3. TESTING:
   - Visit yoursite.netlify.app to test with sample stickers
   - The print dialog will open automatically
   - Set printer to 3x1 inch label paper

SUPPORT:
- Barcode generation: JsBarcode
- Print sizing: 3x1 inches
- Auto-print: Enabled