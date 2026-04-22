# Todoey

A simple iOS to-do list application built with **UIKit** and **Core Data**. The app allows users to create categories, add tasks inside each category, mark tasks as completed, search through tasks, and delete items with swipe actions.

## Screenshots

### Categories Screen
<img width="786" height="1610" alt="Снимок экрана 2026-04-22 в 13 09 06-Photoroom" src="https://github.com/user-attachments/assets/f68434ce-40e6-4af2-a218-385b77415a63" />

### Items Screen
<img width="772" height="1612" alt="Снимок экрана 2026-04-22 в 13 09 19-Photoroom" src="https://github.com/user-attachments/assets/68f1ae1b-8b1d-47bc-812c-8a1558416ce8" />

### Swipe to Delete
<img width="782" height="1620" alt="Снимок экрана 2026-04-22 в 13 09 32-Photoroom" src="https://github.com/user-attachments/assets/3d56ac7a-f95e-48a0-a242-ac094b3a99e7" />

### Search
<img width="776" height="1618" alt="Снимок экрана 2026-04-22 в 13 10 07-Photoroom" src="https://github.com/user-attachments/assets/9fbe8be2-719a-401f-95c1-bdb2cc1ca91b" />

## Features

- Create and save task categories
- Assign a persistent color to each category
- Open a category and manage its tasks
- Mark tasks as done or undone
- Search tasks by title
- Delete categories and tasks with swipe actions
- Gradient-style task list based on the selected category color
- Dynamic navigation bar styling based on the active category

## Tech Stack

- Swift
- UIKit
- Core Data
- Chameleon
- SwipeCellKit
- Xcode Storyboards
- Swift Package Manager

## Project Structure

```text
Todoey
├── Controllers
│   ├── CategoryViewController.swift
│   ├── TodoListViewController.swift
│   └── SwipeTableViewController.swift
├── Data Model
│   └── DataModel.xcdatamodeld
├── Supporting Files
│   ├── Assets.xcassets
│   └── LaunchScreen.storyboard
├── Views
│   └── Base.lproj
├── AppDelegate.swift
└── Info.plist
```

## Core Functionality

### Categories

Users can create custom categories for organizing tasks. Each category is assigned a random color when created, and that color is saved in Core Data so it stays the same after relaunching the app.

### Tasks

Each task belongs to a selected category. Tasks can be added, displayed, updated, and deleted.

### Search

The app supports filtering tasks by title using `UISearchBar` and `NSPredicate`.

### Swipe Actions

Reusable swipe-to-delete logic is implemented in a base controller (`SwipeTableViewController`) and inherited by the other table view controllers.

## Data Persistence

The app uses Core Data for local persistence.

### Main entities

**Category**
- `name: String`
- `color: String`
- relationship: `items`

**Item**
- `title: String`
- `done: Bool`
- relationship: `parentCategory`

## What I Practiced

- Working with Core Data entities and relationships
- Saving and fetching data with `NSFetchRequest`
- Filtering data with `NSPredicate`
- Reusable controller inheritance
- Customizing `UINavigationBarAppearance`
- Building dynamic UI based on stored data
- Integrating third-party libraries with Swift Package Manager

## How to Run

1. Clone the repository
2. Open the project in Xcode
3. Resolve Swift Package Manager dependencies
4. Build and run on Simulator

## Notes

This project was created as part of iOS development practice and was inspired by the App Brewery iOS course. The implementation, UI customization, and Core Data integration were completed independently as part of my learning process.

## Author

**Arina Agafonova**
