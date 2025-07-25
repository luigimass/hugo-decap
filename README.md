# Hugo + Decap CMS Starter

This is a simple Hugo project integrated with Decap CMS, configured for local development.

---

## Prerequisites

- [Hugo](https://gohugo.io/installation/linux/) installed on your machine (if you are using WSL or Linux)

- [Node.js](https://nodejs.org/) installed (needed to run Decap CMS server)

---

## Getting Started

### 1. Install Hugo

Check if Hugo is installed:

```bash
hugo version
```

If not installed, follow the [official Hugo installation guide for Linux](https://gohugo.io/installation/linux/).

---

### 2. Run Hugo server (to preview your site)

In the project root, run:

```bash
hugo server
```

This will start a local web server, usually at:

```
http://localhost:1313
```

You can open this URL in your browser to preview your website content.

---

### 3. Install and run Decap CMS local backend server

To run Decap CMS locally, you need to install `decap-server`. You can install it globally with:

```bash
npm install -g decap-server
```

Or you can run it directly without installing globally via npx:

```bash
npx decap-server
```

This will start the Decap CMS backend server at:

```
http://localhost:8081
```

---

### 4. Run Hugo server and Decap CMS server concurrently

**Important:** You need to run **both** the Hugo server and the Decap CMS backend server at the same time for the CMS to work correctly.

This means:

- Open one terminal window/tab and run:

  ```bash
  hugo server
  ```

- Open a **separate** terminal window/tab and run:

  ```bash
  npx decap-server
  ```

---

### 5. Access the Decap CMS admin interface

Once both servers are running, open the CMS admin interface in your browser at:

```
http://localhost:1313/admin/
```

Here you can log in and start managing your content.

---

## Notes

- Make sure Hugo server (`hugo server`) is running while editing content, so you can preview changes live.
- The CMS configuration assumes `local_backend: true` in your `config.yml` so it works with the local Decap server.

---
