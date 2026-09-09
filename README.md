# Christoffel's Kitchen - Chef's Digital Menu App

**Developer:** Rayan Jaymar Bvulani

**Student Number:** ST10497168

**Group:** 15

**Course:** Higher Certificate In Mobile And Web App Development

**Subject:** Mobile App Scripting

## Links

**GitHub Repository:** [Insert your repository link here]

## Project Overview

The app "Christoffel's Kitchen" is a mobile application developed as part of a practicum in the Mobile App Scripting subject. This application was created using React Native and Expo. The app's primary purpose is to give Chef Christoffel a digital menu he can browse, search, and manage on the go, organised by course (Appetizers, Main Course, Dessert).

The app was developed to meet the requirements of the assignment, which includes creating a functional, navigable mobile app with screens that connect together and share live data between them.

## Purpose and Features

**Purpose:**

The purpose of "Christoffel's Kitchen" is to give Chef Christoffel a simple digital menu system he can update from his phone, instead of relying on a static, printed menu. Dishes can be searched, browsed by category, priced, described, edited, and switched on or off the active menu — all from within the app.

**Key Features:**

- **Splash Screen:** Branded entry point showing the Christoffel's Kitchen logo while the app loads

- **Login Screen:** Email and password fields with input validation before a user can reach the menu

- **Full Menu Screen:** Search bar to find a dish by name across all categories, plus category buttons (Appetizers, Main Course, Dessert) to browse

- **View Average Price:** Calculates and displays the live average price across every dish currently active on the menu

- **Item Detail Screen:** Shows a dish's full name, price, and description

- **Add / Remove from Menu:** Lets the user toggle whether a dish is currently active on the menu, with the Full Menu screen updating immediately to reflect the change

- **Edit Menu Items:** Lets the user edit a dish's name, price, and description in place, with input validation before saving

- **Shared App State:** All screens read from and update the same menu data via React Context, so changes made on one screen are reflected everywhere else instantly

## Design Considerations

The design of Christoffel's Kitchen was based on the following key considerations:

**User Experience (UX):** The app follows a simple, linear flow — Splash, Login, Menu, Item Detail — so the user always knows where they are and how to get back.

**Intuitive Navigation:** Clear navigation using React Navigation's native stack navigator for smooth transitions between screens.

**Visual Hierarchy:** Consistent use of a navy and grey colour scheme, rounded buttons, and an italic serif logo font to give the app a clean, restaurant-appropriate look.

**Form Validation:** Both the Login screen and the Edit Dish form validate input (email format, minimum password length, non-empty fields, valid price) before allowing the user to proceed.

**Performance:** Menu data is held in a single shared context rather than being duplicated across screens, so updates (add, remove, edit) stay in sync without extra re-fetching.

**Accessibility:** Clear touch targets, readable font sizes, and status text (e.g. "Active on menu" / "Not currently on menu") so state is never ambiguous.

## GitHub and GitHub Actions

This project was managed using GitHub for version control, where all code changes were committed and pushed regularly. GitHub enabled an organised development workflow, allowing project integrity to be maintained and progress tracked throughout development.

**GitHub Usage:**

- Regular commits with descriptive messages
- Proper branch management for feature development
- Comprehensive README documentation
- Code organised into `screens/`, `context/`, and `data/` folders

## Screenshots

**App Screenshots:**

**Splash Screen:** Branded entry point with app logo

*[Insert screenshot here — not yet captured]*

**Login Screen:** Email and password entry with validation

![Login Screen](screenshots/login-screen.png)

**Full Menu Screen:** Category browsing, search, and average price

![Full Menu - Categories](screenshots/full-menu-screen.png)

![Full Menu - Appetizers List](screenshots/full-menu-category-list.png)

![Full Menu - Average Price](screenshots/full-menu-average-price.png)

**Item Detail Screen:** Dish info, Add/Remove buttons, and inline editing

![Item Detail](screenshots/item-detail-screen.png)

![Item Detail - Edit Mode](screenshots/item-detail-edit-mode.png)

![Item Detail - After Edit](screenshots/item-detail-after-edit.png)

## Video Demo

*[Insert unlisted YouTube link here]*

## Challenges and Learnings

During the development of this project, several challenges came up:

**Expo SDK version mismatches:** Expo Go on a physical device tracks the newest SDK, which can be ahead of the SDK pinned in the project's `package.json`.

*Solution:* Updated dependencies to match the current SDK and used `npx expo install --fix` to keep every package version aligned automatically going forward.

**Dependency resolution conflicts:** A peer dependency mismatch between `react` and `react-native` versions blocked `npm install`.

*Solution:* Adjusted the pinned version ranges so npm could resolve a compatible set, with `--legacy-peer-deps` as a documented fallback.

**Shared state across screens:** Keeping the menu list in sync across the Full Menu and Item Detail screens as items were added, removed, or edited.

*Solution:* Implemented a `MenuContext` provider so every screen reads and writes the same shared state instead of passing data manually between screens.

**In-place editing:** Adding the ability to edit a dish without a separate screen or losing the existing Add/Remove functionality.

*Solution:* Added a toggleable edit mode on the Item Detail screen itself, with its own validation and Save/Cancel actions.

From these challenges, valuable lessons were learned in React Native/Expo project setup, dependency management, React Context for shared state, and building forms with proper validation.

## Future Enhancements

Potential future enhancements for Christoffel's Kitchen include:

- **Persistent Storage:** Save menu data between sessions using AsyncStorage or SQLite
- **Real Authentication:** Connect the Login screen to a real authentication service (e.g. Firebase)
- **Image Support:** Allow a photo to be added for each dish
- **Role Toggle:** Separate Chef (edit) and Client (view-only) modes
- **Advanced Filtering:** Add price-range filters alongside the existing search
- **Offline Support:** Allow menu browsing without an internet connection
- **Backend Integration:** Sync menu data across multiple devices via a cloud database

These enhancements would improve the app's usability and make it more suitable for real restaurant use.

## References

- React Native Documentation: https://reactnative.dev/docs/getting-started
- React Navigation Documentation: https://reactnavigation.org/docs/getting-started
- Expo Documentation: https://docs.expo.dev/

## List of Figures

1. Splash Screen Design: Initial loading screen with app branding
2. Login Screen Layout: Email/password entry with validation
3. Full Menu Interface: Search, category browsing, and average price
4. Item Detail Screen: Dish info, Add/Remove, and inline editing

