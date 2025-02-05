# Broken Save System
After running the game, the save system may be broken and always return false when getting key in Storager.

It IS fixable, here is how:

Go to Storager and find method called `hasKey(string key)`	
And at start of the method add this:
```
if (Application.isEditor) return PlayerPrefs.HasKey(key);
```

This will fix the loading issue.