# TaskFlow

A clean, fast, premium to-do list built with plain HTML, CSS, and vanilla JavaScript. The whole app lives in a single `index.html` file. There is no backend, no database, no build step, and no paid API.

Tasks are saved in your browser with `localStorage`, so they are still there when you come back.

## Features

- Add, edit, complete, and delete tasks
- Low, Medium, and High priority with colour-coded badges
- Optional due dates, with an "Overdue" badge for late tasks
- Filter by All, Active, or Completed
- Live counts for Total, Remaining, and Completed tasks
- Automatic saving with `localStorage`
- Confirmation dialog before clearing completed tasks or all tasks
- Blue-and-white interface that adapts to phones, tablets, and desktops
- Validation for empty input, with clear error messages
- Accessible labels, visible focus outlines, and full keyboard support
  - `Enter` saves an edit
  - `Esc` cancels an edit

## Tech stack

| Part | Technology |
| --- | --- |
| Markup | HTML5 |
| Styling | CSS3 (custom properties, grid, flexbox) |
| Logic | Vanilla JavaScript (no frameworks, no libraries) |
| Storage | Browser `localStorage` |
| Hosting | Vercel (static site) |

## Project structure

```
taskflow/
├── index.html   # the complete app (HTML + CSS + JS)
└── README.md    # this file
```

## Run it locally

No installation needed.

1. Download or clone the repository.
2. Double-click `index.html` to open it in your browser.

Optional: to serve it from a local web server instead, run this in the project folder (requires Python):

```bash
python3 -m http.server 8000
```

Then open <http://localhost:8000>.

## Deploy to Vercel

1. Push this repository to GitHub, with `index.html` at the top level (not inside a folder).
2. Sign in at [vercel.com](https://vercel.com) with GitHub.
3. Click **Add New → Project** and import the `taskflow` repository.
4. Set **Framework Preset** to **Other**.
5. Leave **Build Command**, **Output Directory**, and **Install Command** empty.
6. Click **Deploy**.

Every time you commit a change to GitHub, Vercel redeploys automatically.

## Keyboard shortcuts

| Key | Action |
| --- | --- |
| `Tab` / `Shift + Tab` | Move between controls |
| `Enter` | Add a task, or save while editing |
| `Space` | Toggle a task's checkbox |
| `Esc` | Cancel editing or close the confirmation dialog |

## Data and privacy

- All data stays in your own browser. Nothing is sent to any server.
- Tasks do not sync between devices or browsers.
- Clearing your browser's site data for this page will erase your saved tasks.
- The storage key used is `taskflow.tasks.v1`.

## Browser support

Works in current versions of Chrome, Edge, Firefox, and Safari. The confirmation dialog uses the native `<dialog>` element, with a built-in fallback for older browsers.

## Customising

- **Colours:** edit the CSS variables at the top of the `<style>` block in `index.html` (for example `--blue-600`).
- **Storage key:** change the `KEY` value in the script if you want to reset saved data for a new version.

## License

Free to use, modify, and share. Add a `LICENSE` file (for example MIT) if you want to set formal terms.
