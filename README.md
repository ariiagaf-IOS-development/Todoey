# Todoey

A simple iOS to-do list application built with **UIKit** and **Core Data**. The app allows users to create categories, add tasks inside each category, mark tasks as completed, search through tasks, and delete items with swipe actions.

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
