# Go Wiki

This is a simple web-based wiki written in Go, following the [Go Wiki Tutorial](https://go.dev/doc/articles/wiki/). 

The project has been modified with a new file structure. 
- `data/` directory for storing page content and 
- `templates/` for HTML views.

## File Structure

```
├── data/
│   ├── test1.txt
│   └── test2.txt
├── go.mod
├── README.md
├── simple-webserver.go
├── templates/
│   ├── edit.html
│   └── view.html
└── wiki.go
```

## Running Locally

### Requirements

- [Go](https://golang.org/dl/) 1.18 or higher

### Run the Server

```bash
go run main.go
```

The server will start on port `8000`. Open your browser and navigate to:

```
http://localhost:8000/view/YourPageName
```

If the page doesn't exist, you will be redirected to the edit screen to create it.

## Routes

- `/view/{PageTitle}` – View a page
- `/edit/{PageTitle}` – Edit a page

## Templates

The app uses two templates:

- `view.html` – Displays saved content
- `edit.html` – Provides a form to edit content

## Notes

- Page titles can only include alphanumeric characters (`a-z`, `A-Z`, `0-9`)
- All pages are stored as `.txt` files in the `data/` directory

## License

This project is derived from the [Go Wiki example](https://go.dev/doc/articles/wiki), which is licensed under the BSD 3-Clause License © 2009 The Go Authors.

Modifications and additional work are licensed under the MIT License © 2025 ABurntBagel.

See [LICENSE](LICENSE) for full details.
