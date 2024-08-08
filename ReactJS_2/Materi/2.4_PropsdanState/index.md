Pengertian:
Props (Properties): Digunakan untuk mengirim data dari satu komponen ke komponen lain, terutama dari komponen induk ke komponen anak. Props bersifat read-only.
State: Mengelola data yang dapat berubah dan mempengaruhi tampilan UI di dalam komponen. Dalam function components, state dikelola menggunakan useState hook.
Contoh:

Props:
// Komponen fungsi "Welcome" menerima props dan menggunakan nilainya
function Welcome(props) {
  // Mengembalikan elemen h1 yang menampilkan teks dengan props.name
  return <h1>Selamat datang, {props.name}!</h1>;
}

// Merender komponen "Welcome" dengan props name bernilai "Mirza"
ReactDOM.render(<Welcome name="Mirza" />, document.getElementById('root'));
State dengan useState:
// Mengimpor React dan useState hook
import React, { useState } from 'react';

// Mendefinisikan komponen fungsi bernama "Counter"
function Counter() {
  // Mendefinisikan state "count" dengan nilai awal 0
  const [count, setCount] = useState(0);

  // Fungsi untuk menambah nilai "count" ketika tombol ditekan
  const increment = () => {
    // Menggunakan fungsi setCount untuk mengupdate nilai count
    setCount(count + 1);
  }

  // Mengembalikan elemen JSX dengan nilai count dan tombol untuk menambah count
  return (
    <div>
      <h1>Hitungan: {count}</h1>
      <button onClick={increment}>Tambah</button>
    </div>
  );
}

// Merender komponen "Counter" ke dalam elemen dengan id "root"
ReactDOM.render(<Counter />, document.getElementById('root'));