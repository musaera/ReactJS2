Pengertian:
Functional Components adalah komponen React yang ditulis sebagai fungsi JavaScript yang menerima props dan mengembalikan elemen React.
Contoh:

// Mendefinisikan komponen fungsi bernama "Greeting"
function Greeting(props) {
  // Menggunakan props untuk mengambil data dan mengembalikan elemen h1 dengan teks yang dipersonalisasi
  return <h1>Halo, {props.name}!</h1>;
}

// Merender komponen "Greeting" dengan mengirimkan properti "name" sebagai props
ReactDOM.render(<Greeting name="Mirza" />, document.getElementById('root'));