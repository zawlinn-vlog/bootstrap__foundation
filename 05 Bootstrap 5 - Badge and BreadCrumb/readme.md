### Badge &mdash;

#### How to badge in HTML &mdash;

```html
<span class="badge rounded-pill text-bg-primary">Primary</span>
<span class="badge rounded-pill text-bg-secondary">Secondary</span>
<span class="badge rounded-pill text-bg-success">Success</span>
<span class="badge rounded-pill text-bg-danger">Danger</span>
<span class="badge rounded-pill text-bg-warning">Warning</span>
<span class="badge rounded-pill text-bg-info">Info</span>
<span class="badge rounded-pill text-bg-light">Light</span>
<span class="badge rounded-pill text-bg-dark">Dark</span>
```

#### How to create noti with badge &mdash;

```html
<button type="button" class="btn btn-primary">
  Notifications <span class="badge text-bg-secondary">4</span>
</button>
```

OR

```html
<button type="button" class="btn btn-primary position-relative">
  Inbox
  <span
    class="position-absolute top-0 start-100 translate-middle badge rounded-pill bg-danger"
  >
    99+
    <span class="visually-hidden">unread messages</span>
  </span>
</button>
```

OR

```html
<button type="button" class="btn btn-primary position-relative">
  Profile
  <span
    class="position-absolute top-0 start-100 translate-middle p-2 bg-danger border border-light rounded-circle"
  >
    <span class="visually-hidden">New alerts</span>
  </span>
</button>
```

#### BreadCrumb &mdash;

```html
<ul
    class="breadcrumb" style="--bs-breadcrumb-divider: url(&#34;data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='8' height='8'%3E%3Cpath d='M2.5 0L1 1.5 3.5 4 1 6.5 2.5 8l4-4-4-4z' fill='%236c757d'/%3E%3C/svg%3E&#34)
        "
      >
    <li class="breadcrumb-item">
        <a href="#" class="text-decoration-none">Home</a>
    </li>
    <li class="breadcrumb-item">
        <a href="#" class="text-decoration-none">Library</a>
    </li>
    <li class="breadcrumb-item active">Data</li>
</ul>
```
