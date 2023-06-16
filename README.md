# Command Exists
This is a simple Github Action to check if a command exists in the current environment.

## Usage
```yaml
  steps:
    # …
    - name: Check if git exists
      uses: kpbode/command-exists@v1
      id: check-command-exists
      with:
        command: 'git'
    - name: Do something if git exists
      if: steps.check-command-exists.outputs.exists == 'true'
      run: echo "git exists"
    # …
```

