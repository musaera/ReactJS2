Pengertian:
Conditional rendering memungkinkan Anda merender komponen atau elemen berdasarkan kondisi tertentu, menggunakan ekspresi JavaScript seperti if, else, dan ternary operator.
Contoh:

// Mendefinisikan komponen fungsi bernama "Greeting"
function Greeting(props) {
  // Menggunakan operator ternary untuk memutuskan teks yang akan dirender berdasarkan nilai props.isLoggedIn
  const isLoggedIn = props.isLoggedIn;
  return (
    <div>
      {isLoggedIn ? (
        <h1>Selamat datang kembali!</h1>
      ) : (
        <h1>Silakan login.</h1>
      )}
    </div>
  );
}

// Merender komponen "Greeting" dengan props isLoggedIn bernilai false
ReactDOM.render(<Greeting isLoggedIn={false} />, document.getElementById('root'));