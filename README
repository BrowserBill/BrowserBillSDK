# BrowserBill

## Description

[BrowserBill](https://browserbill.com) is a full-featured browser extension billing platform. It provides all of the necessary features to allow for browser extension monetisation.

This repository contains the BrowserBill SDK which needs to be embedded into the browser extension to allow for payments to be accepted and facilitate important operations.

You will also find other helpful resources such as a tutorial and example extensions.

## Tutorial

### 1. Copy SDK into source code
Copy the `BrowserBillSDK.js` file into your extension's source code. 

### 2. Update manifest
Update your extension's `manifest.json` file to include `storage` permission as follows:

```
...
"permissions": [
    "storage"
]
...
```

### 3. For pop-up access
If you want to access the SDK in your pop-up then you will need to include the SDK in your pop-up's HTML file as follows:

```
<script src="BrowserBillSDK.js"></script>
```

This is commonly placed just before the closing `</body>` tag.

### 4. For background access
If you want to access the SDK in your background script then you will need to include the following line at the top of the file:

```
importScripts('BrowserBillSDK.js');
```

### 5. Create instance of BrowserBill
Now that the pop-up or background script has access to the SDK, you can create an instance of it with the following:

```
var bb = new BrowserBill('EXTENSION_CODE');
```

Where `EXTENSION_CODE` is replaced with your extension's code that you created on the website (e.g. 'my-extension'). If you have not created an extension yet, create one on the [BrowserBill](https://browserbill.com) website and return here.

### 6. Get user info
To get information about the user, such as whether they have paid or the plan that they have purchased, you can use the `getUser()` method as follows:

```
bb.getUser().then((data) => {
    console.log(data.paid)
});
```

### 7. Direct the user to checkout
To direct the user to the checkout page, you can use the `openPaymentPage()` method as follows:

```
bb.openPaymentPage('PLAN_ID');
```

Where `PLAN_ID` is replaced with your plan's ID as found on the BrowserBill website dashboard.

## Example

You can find an example extension created with the BrowserBill SDK in the `/example` folder. There are examples created for Manifest V2 and V3 in the folders titled `mv2` and `mv3` respectively.

To try these, simply go to your extensions page in your browser, enable developer mode and load your preferred extension. You can edit the code to have it work with your extension and plan by updating the `popup.js` file.

## Complete Reference

### getUser()
Gets information about the user such as their paid status and the plan they purchased.

Example response:

```
{
    paid: true,
    plan: 1
}
```

### openPaymentPage(PLAN_ID)
Opens the payment page for the provided plan so the user can checkout.

### openManagementPage()
Opens the purchase management page so the user can view and manage their purchases.

### openLoginPage()
Opens the login page for the user if they want to login from a new device. Note that the user can also access the login page from the payment page.

## Links
- Website: [https://browserbill.com](https://browserbill.com)
- Getting started tutorial: [https://browserbill.com/getting-started](https://browserbill.com/getting-started)

## License
The BrowserBill SDK license can be found [here](https://github.com/BrowserBill/BrowserBillSDK/blob/main/LICENSE).