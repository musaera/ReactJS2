Pengertian:
Event handling di React mirip dengan HTML, namun dengan penamaan (camelCase) dan penggunaan sintaks JSX.
Contoh:

// Mendefinisikan komponen fungsi bernama "ClickButton"
function ClickButton() {
  // Fungsi event handler untuk menampilkan alert saat tombol ditekan
  const handleClick = () => {
    alert('Tombol ditekan!');
  };

  // Mengembalikan elemen tombol yang mengikat event onClick dengan fungsi handleClick
  return (
    <button onClick={handleClick}>
      Tekan Saya
    </button>
  );
}

// Merender komponen "ClickButton" ke dalam elemen dengan id "root"
ReactDOM.render(<ClickButton />, document.getElementById('root'));