# POS Receipt Screen

This Odoo module introduces a **Feedback Screen** to the Point of Sale (POS) interface, designed to display transaction details and manage the post-payment flow.

## Features

- **Transaction Summary**: Clearly displays the following information to the user:
  - **Change**: The amount to be returned to the customer.
  - **Cash**: The amount paid by the customer.
  - **Amount Paid**: The total order amount.
- **Process Management**:
  - Includes a loading state to indicate if background processes are still running.
  - Displays a "Everything is ready to go!" message when processes are complete.
- **Auto-Completion**: Automatically finalizes the order and proceeds after a 5-second timeout once all background tasks are finished.

## Technical Details

- **Component**: `FeedbackScreen`
- **Files**:
  - `feedback_screen/feedback_screen.js`: Logic for the screen, including state management and timeout handling.
  - `feedback_screen/feedback_screen.xml`: QWeb template for the screen layout.
  - `feedback_screen/feedback_screen.scss`: Styling for the feedback screen.

## Installation

To apply these changes, replace the existing files in the Odoo installation with the files from this module.

**Target Directory:**
`C:\Program Files\Odoo 19.0.20251101\server\odoo\addons\point_of_sale/static/src/app/screens/feedback_screen/`

**Action:**
Copy the files from the `feedback_screen/` folder of this module (`feedback_screen.js`, `feedback_screen.xml`, `feedback_screen.scss`) and overwrite the corresponding files in the target directory.

## Usage

This screen is intended to be used in the POS flow, likely triggered after payment to show confirmation and change details before moving to the next order.
