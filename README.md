## UNMAINTAINED ##
This addon is unmaintained and has issues with newer versions of WHMCS / PHP.
Let me know if you would like to contribute by fixing the open issues.


# Credit invoice / credit note addon for WHMCS

A simple module that allows admins to credit / refund invoices.

The module adds buttons to the WHMCS invoice edit page. You can refund an invoice
and easily navigate between it's corresponding credit note.

The module does this by duplicating an invoice, setting it's status to "Paid",
and then inverting all the amounts to negative. Finally it adds some data to both
the original invoice admin notes as well as the credit notes admin notes, this is
to be able to easily keep track of which credit note belongs to which invoice, and vise-versa.

## Installing

1. Download the [latest version](https://github.com/Onlineforce/whmcs-credit-invoice/releases/latest)
2. Extract the archive and copy the __credit_invoice__ folder to whmcs_path/modules/addons
3. Activate the module from the "Addon Modules" settings page.
4. On the same page as above, press "Configure" and choose the admin groups that can create credit notes.

## Usage

Open an invoice. You should see a new button, "Credit invoice". When pressed, a new invoice will be created.

The new invoice will contain the exact same line items, but with reversed amounts _($10 becomes -$10)_.

You will be redirected to the new credit note, where you can send the invoice to your client _(standard WHMCS way)_. It is also possible to navigate between the original and the credit note by pressing the button.

## Todo

* Add development tools with Composer (phpcs, phpcbf, Phan, etc.)
* Add tests
* ~~Use GitHub releases~~
