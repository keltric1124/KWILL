# Kwill — Quail Farm Management System

A web app for managing a quail farm: user accounts, a dashboard of key stats, egg
production tracking, quail population & mortality tracking, feed logging, sales &
expenses, trend charts, and PDF report export.

## System Architecture

Kwill is a server-rendered Node.js/Express app — the browser talks directly to an Express
server that renders EJS pages.Routes hand off to controllers, which query a PostgreSQL database through a pooled
connection, and render views back to the browser. express-session handles login state;
PDF report export uses Puppeteer to render report pages headlessly. Pushing to GitHub triggers Render to automatically rebuild and redeploy the web service.
<img width="1783" height="607" alt="image" src="https://github.com/user-attachments/assets/c723263a-4f8b-4dfd-b66a-6637cdb6be0e" />
