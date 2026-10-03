# Mesa de Ayuda

A small PHP "help desk" style admin dashboard for managing employees (`Empleado`), job positions (`Cargo`), departments/areas (`Area`), and support requests (`Requerimiento`). Built with the [Black Dashboard](https://www.creative-tim.com/product/black-dashboard) Bootstrap admin template for the UI.

## How it works

- `index.php` loads `dashboard.php`, which renders a shared layout (`templates/menu.php`, `header.php`, `footer.php`) and includes a view based on the `?page=` query parameter.
- Each entity has a DAO (`src/dao/*Dao.php`) for data access, a DTO (`src/dto/*Dto.php`) for data transfer, and a view (`src/view/*View.php`) rendering an HTML table.
- Database access goes through a custom lightweight wrapper (`src/shared/Conectar.php`) plus a bundled `ez_sql` MySQL helper library (`lib/`).

## Tech stack

- Plain PHP (no framework), procedural + simple DAO/DTO pattern
- MySQL (via `ez_sql_mysql.php`)
- Black Dashboard (Bootstrap-based admin UI template) for styling

## Running it

Requires a local PHP + MySQL environment (e.g. XAMPP/MAMP) with the database connection configured in `src/shared/Conectar.php`. Place the project in your web server's document root and open `index.php`.

## Context

University/personal coursework project practicing basic CRUD operations and the DAO/DTO pattern in vanilla PHP, using a pre-built admin dashboard template for styling.
