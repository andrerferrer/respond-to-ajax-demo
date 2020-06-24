# GOAL

This is a demo to show-case how to implement AJAX in rails using the [`turbolinks gem`](https://github.com/turbolinks/turbolinks).

[You can also check my other demos](https://github.com/andrerferrer/dedemos/blob/master/README.md#ded%C3%A9mos).

## What needs to be done?

### 1. Add `remote: true` to the link
On your view
```erb
<%= link_to '❌', restaurant, method: :delete, remote: true, data: { confirm: "Are you sure?" } %>
```

### 2. Add to the controller
We'll add the respond_to

```ruby
def destroy
  set_restaurant
  @restaurant.destroy
  respond_to do |format|
    format.js
  end
end
```

### 3. Create the `js.erb` view

In the `destroy.js.erb` we will write the js that will return. With this JS we will remove the element from the DOM.

```js
document.getElementById("restaurant-<%= @restaurant.id %>").remove()
```

And we're good to go 🤓
Good Luck and Have Fun
