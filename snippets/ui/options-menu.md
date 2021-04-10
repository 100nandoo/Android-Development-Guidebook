```kotlin
// layout is inside res.menu.layout_name
override fun onCreateOptionsMenu(menu: Menu, inflater: MenuInflater) {
    inflater.inflate(R.menu.layout_name, menu)
    super.onCreateOptionsMenu(menu, inflater)
}

override fun onPrepareOptionsMenu(menu: Menu) {
    menuItemUpload = menu.findItem(R.id.action_done)
    menuItemUpload.isEnabled = true
    super.onPrepareOptionsMenu(menu)
}

override fun onOptionsItemSelected(item: MenuItem): Boolean {
    when (item.itemId) {
        R.id.action_done -> finish()
    }
    return super.onOptionsItemSelected(item)
}
```