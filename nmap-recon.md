Basic Scanning Techniques
| Command | Description |
|----------|----------|
| ` scan single target  ` |  Scan a single target | <button onclick="copyToClipboard('echo \"Hello\"')">Copy</button>  |
| ``` scan single target  ``` |


<html>

| Command          | Description               |
|------------------|---------------------------|
| `git status`     | List all new or modified files | ```git status ```
| `git diff`      | Show file differences that haven't been staged |
| **Copy Command** | <button onclick="copyToClipboard('git status')">Copy to Clipboard</button> |

<script>
function copyToClipboard(text) {
    navigator.clipboard.writeText(text).then(function() {
        alert('Copied to clipboard: ' + text);
    }, function(err) {
        console.error('Could not copy text: ', err);
    });
}
</script>

</html>







