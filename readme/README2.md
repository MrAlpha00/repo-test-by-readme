# CyberSec Hub 2026

A personal cybersecurity resources dashboard to support my learning journey in 2026.

![Screenshot](screenshots/main.png)

## About

CyberSec Hub is a self-hosted web application that centralizes all my cybersecurity learning resources in one place. It provides quick access to training platforms, news sites, certifications, and security tools.

This project was created to organize my studies and stay up-to-date with the latest cybersecurity trends and resources.

## Features

- **Curated Resources** - Links to training platforms, news, certifications, and tools
- **Category Filtering** - Filter resources by category (All, Training, News, Certifications, Tools)
- **Category Management** - Add, edit, and delete categories directly from the interface
- **Drag and Drop** - Reorder links within any category
- **Admin Panel** - Add or remove links directly from the interface
- **Automatic Icons** - Favicons are downloaded and converted to WebP automatically
- **Open All News** - Open all news sites at once with a single click
- **Dark Theme** - Modern dark interface, easy on the eyes
- **Persistent Storage** - All data is saved to a JSON file

## Screenshots

| Admin Mode |
|------------|
| ![Admin](screenshots/admin.png) |

| Add Link Modal | News Category |
|----------------|---------------|
| ![Modal](screenshots/modal.png) | ![News](screenshots/news.png) |

### Category Management

| Add Category | Edit Category |
|--------------|---------------|
| ![Add Category](screenshots/add-category.png) | ![Edit Category](screenshots/edit-category.png) |

## Installation

### Prerequisites

- Node.js (v14 or higher)
- npm

### Setup

1. Clone the repository

```bash
git clone https://github.com/ShoshinMaster/cybersec-hub-2026.git

cd cybersec-hub-2026
```

2. Install dependencies

```bash
npm install
```

3. Start the server

```bash
node server.js
```

4. Open your browser at `http://localhost:3000`

## Usage

### Navigation

Click on category tabs to filter resources:
- **All** - Display all resources
- **Training** - Learning platforms and courses
- **News** - Cybersecurity news and blogs
- **Certifications** - Professional certifications
- **Tools** - Security tools and frameworks

### Admin Mode

1. Click the gear icon (top right) to enter admin mode
2. The icon turns red when admin mode is active
3. Click "+" to add a new link
4. Click "x" on any card to delete a link
5. Click the gear icon again to exit admin mode

### Category Management

1. Enter admin mode (click the gear icon)
2. Click the green "+" button next to the category tabs to add a new category
3. Double-click on any existing category tab to edit or delete it
4. Enter the category name and click "Save"
5. To delete a category, click "Delete" in the edit modal

> **Note:** Deleting a category will also delete all links within that category.

### Adding a Link

1. Enter admin mode
2. Click the "+" card
3. Fill in the name, URL, and category
4. Click "Save"
5. The favicon is downloaded automatically

### Open All News Links

When you click the "Open All" button on the News page, your browser may block the pop-ups. To allow multiple tabs to open:

1. Click the "Open All" button
2. Your browser will show a pop-up blocked notification
3. Click on the notification and select "Always allow pop-ups from localhost:3000"
4. Click "Done" and try again

![Pop-up Settings](screenshots/popup-allow.jpg)

> **Note:** This is a browser security feature to prevent unwanted pop-ups. You only need to allow it once.


## Project Structure

```
cybersec-hub-2026/
├── app.js                  # Frontend JavaScript
├── data.json               # Links database
├── categories.json         # Categories database
├── download-icons.js
├── icons                   # Downloaded favicons (WebP)
│   └── ....webp
├── index.html              # Main HTML file
├── package.json
├── package-lock.json
├── README.md               # This file
├── screenshots             # Project screenshots
│   └── ....png
├── server.js               # Node.js server with API
├── styles.css              # Stylesheet
└── UNLICENSE
```

## API Endpoints

| Method | Endpoint | Description |
|--------|----------|-------------|
| GET | `/api/data` | Get all links |
| POST | `/api/data` | Save all links |
| POST | `/api/add` | Add a new link (downloads icon) |
| POST | `/api/delete` | Delete a link and its icon |
| GET | `/api/categories` | Get all categories |
| POST | `/api/categories/add` | Add a new category |
| POST | `/api/categories/update` | Update a category |
| POST | `/api/categories/delete` | Delete a category |

## Technologies

- HTML5
- CSS3
- Vanilla JavaScript
- Node.js
- Sharp (image processing)

No frameworks or external libraries on the frontend.

## License

This project is released into the public domain.

You are free to use, modify, distribute, and build upon this project for any purpose, without any restrictions.

**This is free and unencumbered software released into the public domain.**

See the [UNLICENSE](UNLICENSE) file for details.

## Acknowledgments

Thanks to all the cybersecurity platforms, educators, and communities that provide valuable resources for learners worldwide.