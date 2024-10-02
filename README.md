# iBukas Inc.

This is an attempt to build an investment broker that automatically adds percentage in form of profit to investors account. The Mobile App uses certain logic to handle complex ideas, but overall maintaining a simple codebase.


## Technologies Used

- [React Native](https://reactnative.dev/) - Framework for building native mobile apps using React.
- [Firebase](https://firebase.google.com/) - Backend platform for authentication, database, and hosting.
- [Firestore](https://firebase.google.com/products/firestore) - NoSQL database to store and sync data in real-time.
- [Bootstrap](https://getbootstrap.com/) - CSS framework for responsive design and component styling.
- [FontAwesome](https://fontawesome.com/) - Icon library for adding scalable vector icons to your app.
- [Expo](https://expo.dev/) - Platform for developing and deploying React Native apps.


## App Version Control

The firestore collection that holds the wallets has a data string `requiredVersion` which is a number signifying the required version number for it to run properly.

In the App.jsx, there is a  `const currentVersion = "1"` then an if statement for when the  `currentVersion === requiredVersion`, then the main app will display, else it will display a screen prompting to download a newer version to use.


## Investment Trade & Profit Logic

To handle Investment Trades, user enters an amount and if it falls within the minimum and maximum of any plan, it selects the plan and displays the duration and hourly profit.

When the trade starts with `$200` for example, it gives a `24 hours` duration and `$30` per hour profit; the logic then takes `24 x 30 = 720` as the profit and automatically at it to the user balance. New trades and withdrawals is then disabled, till the end of the 24 hours.


## Withdrawal Logic
Withdrawal is disabled for investors, ie when your trade is still active. If trade is not active, then user has to fill in form and submit.

If the user account is active then a success message comes up and the transaction is logged into the system.

If user account is deactivated, it will request an Authentication code to complete transactions, this is a simple way to handle withdrawal in case of fees.

## Future Features

The project is open to future upgrades, kindly send a DM to suggest.
