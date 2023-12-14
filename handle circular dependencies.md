- Circular dependencies happen when two modules must call into each other at import time. They can cause your program to crash at startup.

- The best way to break a circular dependency is by refactoring mutual dependencies into a separate module at the bottom of the dependency tree.

- Dynamic imports are the simplest solution for breaking a circular dependency between modules while minimizing refactoring and complexity.
```python
# dialog.py

class Dialog:

	...

save_dialog = Dialog()

def show():

	import app # Dynamic import

	save_dialog.save_dir = app.prefs.get('save_dir')

...
```