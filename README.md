\`\`\`bash
sudo bash -c "$(curl -sL https://github.com/Gozargah/Marzban-scripts/raw/master/marzban.sh)" @ install
\`\`\`
<button onclick="copyToClipboard()">Copy</button>

<script>
function copyToClipboard() {
  var copyText = document.querySelector("code").textContent;
  navigator.clipboard.writeText(copyText).then(function() {
    alert('Copied to clipboard');
  }, function(err) {
    alert('Failed to copy');
  });
}
</script>
