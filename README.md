<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta http-equiv="X-UA-Compatible" content="IE=edge">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <style>
    .square {
      float: left;
      width: 10px;
      height: 10px;
      margin: 2px;
    }
    .gray {
      background-color: lightgray;
    }
    .darkgray {
      background-color: darkgray;
    }
  </style>
  <title>Squares</title>
</head>
<body>
  <table>
    <tbody>
    </tbody>
  </table>
  <script>
    for (let i = 1; i <= 100; i++) {
      let square = document.createElement('div');
      square.className = 'square';
      if (i % 2 === 0) {
        square.style.border = '1px solid black';
        square.classList.add('gray');
      } else {
        square.style.width = '20px';
        square.style.height = '20px';
        square.classList.add('darkgray');
      }
      document.querySelector('table > tbody').appendChild(square);
      if (i % 10 === 0) {
        document.querySelector('table > tbody').appendChild(document.createElement('br'));
      }
    }
  </script>
</body>
</html>
