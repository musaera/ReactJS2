Pengertian:
React adalah library JavaScript untuk membangun user interfaces, terutama single-page applications (SPA) yang memerlukan update data dinamis tanpa refresh seluruh halaman.
Contoh:

<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>React App</title>
</head>
<body>
  <!-- Elemen ini adalah tempat React akan merender komponen -->
  <div id="root"></div>

  <!-- Menyertakan React dan React DOM -->
  <script src="https://unpkg.com/react@17/umd/react.development.js" crossorigin></script>
  <script src="https://unpkg.com/react-dom@17/umd/react-dom.development.js" crossorigin></script>

  <!-- React Script -->
  <script>
    // Mendefinisikan komponen fungsi bernama "Welcome"
    function Welcome() {
      // Komponen ini mengembalikan elemen h1 yang berisi teks "Hello, React!"
      return <h1>Hello, React!</h1>;
    }

    // Merender komponen "Welcome" ke dalam elemen dengan id "root"
    ReactDOM.render(<Welcome />, document.getElementById('root'));
  </script>
</body>
</html>