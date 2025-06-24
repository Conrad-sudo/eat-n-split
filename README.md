Here is a professional and clear `README.md` for your **eat-n-split** React application:

---

# 🍽️ eat-n-split

**eat-n-split** is a simple and interactive React application that allows users to manage shared expenses with friends by splitting bills and tracking balances. Whether you're dining out or sharing costs, this app helps you figure out who owes what.

---

## 🚀 Features

* Add new friends with custom avatars
* Select a friend to split a bill with
* Enter the total bill and who paid what
* Automatically updates balances between you and your friends
* Clear UI feedback on who owes who
* Toggle friend selection and form visibility

---


## 🛠️ Tech Stack

* React (with Hooks)
* Functional components
* Local state management using `useState`

---

## 💻 How It Works

### 🧠 Application State

The app uses `useState` to manage:

* `friends`: A list of friends and their balances
* `showAddFriend`: Toggles the "Add Friend" form
* `selectedFriend`: Tracks which friend is currently selected

### 🔗 Component Overview

#### `App`

The root component that controls layout and state logic. It handles:

* Adding friends
* Selecting a friend
* Toggling forms
* Splitting a bill

#### `FriendsList`

Displays a list of all current friends using the `Friend` component. Handles selection logic.

#### `Friend`

Shows an individual friend with their:

* Avatar
* Name
* Balance status (who owes whom)
* Button to select or deselect the friend

#### `FormSplitBill`

Allows the user to:

* Enter the total bill
* Specify how much they paid
* Automatically calculates how much the friend paid
* Choose who paid the bill
* Submits the split and updates balances

#### `FormAddFriend`

Form to add a new friend with:

* Name
* Avatar image URL
* Auto-generated unique ID and starting balance of `$0`

#### `Button`

Reusable styled button component.

---

## 💰 Balance Logic

* A **positive balance** means the friend **owes you**.
* A **negative balance** means **you owe the friend**.
* A **zero balance** means you're **even**.

When a bill is split:

* If **you paid**, the friend’s balance increases.
* If **they paid**, the friend’s balance decreases.

---

## 📦 Getting Started

### 1. Clone the repo

```bash
git clone https://github.com/yourusername/eat-n-split.git
cd eat-n-split
```

### 2. Install dependencies

```bash
npm install
```

### 3. Run the development server

```bash
npm start
```

Visit `http://localhost:3000` to use the app.

---

## 📂 Project Structure

```
src/
│
├── App.js              # Main app component
├── index.js            # Entry point
├── components/         # (You can move reusable components here)
└── styles.css          # (Optional) Styling
```

---

## 🔮 Future Improvements

* Persist data with local storage or a backend
* Allow editing/removing friends
* Add support for group bill splitting
* Mobile-friendly responsive design
* Currency formatting and localization

---

## 🧹 Known Limitations

* Data is not saved between sessions
* Limited to one-on-one bill splits

---

## 📄 License

This project is open source and available under the [MIT License](LICENSE).

