# GOAL

This is a demo to show-case how to implement AJAX in rails using the [`turbolinks gem`](https://github.com/turbolinks/turbolinks).

[You can also check my other demos](https://github.com/andrerferrer/dedemos/blob/master/README.md#ded%C3%A9mos).

## What needs to be done?

### 1. Add the gem
```ruby
# Gemfile
gem 'turbolinks'
```
Remember to `bundle install`

### 2. Require turbolinks in your JS
In your [`application.js`]()
```js
require("turbolinks").start()

// ...

// Remember to call your functions here
document.addEventListener('turbolinks:load', () => {
});
```

### 3. Add `remote: true`
In the [view]()

```erb
<%= link_to '❌', restaurant, method: :delete, remote: true, data: { confirm: "Are you sure?" } %>
```

### 4. Troubleshooting
If nothing happens, remember to `redirect_to` something in your controller


And we're good to go 🤓
Good Luck and Have Fun
