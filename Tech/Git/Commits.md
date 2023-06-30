## Name style for Git Commits
1) ADD: list of new files - description of added functionality
    ```
    ADD: authorize.py - add google auth
    ```
2) UPDATE: list of changed files (most important) - list of changes
    ```
    UPDATE: aythorize.py - change google auth to discord, delete get_ip method
    ```
3) DELETE: list of deleted files (most important) - reason
    ```
    DELETE: aythorize.py - it's deprecated logic
    ```
4) FIX: bug name - describe reason
    ```
    FIX: discord auth cycle - invalid token
    ```
5) RELEASE: version - most changes
    ```
    RELEASE: v0.1.2 - add (discord, google auth), improve load perfomance
    ```

### Recommendations
1) 1 action = 1 commit
2) More commits is better than none
3) Commit must not include many  changes
4) Good commit name helps avoid confusion

[You can find more about the style of commits in my repos](https://github.com/BaggerFast)