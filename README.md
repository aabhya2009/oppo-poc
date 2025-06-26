<!DOCTYPE html>
<html>
<head>
  <meta charset="utf-8">
  <title>OPPO XSS + CORS PoC</title>
</head>
<body>
  <h3>OPPO XSS + CORS PoC</h3>
  <p>Edit the <code>thirdpartytype</code> parameter in the URL to inject payloads.</p>
  <script>
    const params = new URLSearchParams(window.location.search);
    const third = params.get('thirdpartytype');
    if (third) {
      document.body.innerHTML += third; // This simulates the vulnerable rendering behavior
    }
  </script>
</body>
</html>#
