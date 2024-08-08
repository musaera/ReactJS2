Pengertian:
Ketika merender daftar elemen, Anda perlu memberikan key yang unik pada setiap elemen untuk membantu React mengidentifikasi elemen mana yang telah berubah.
Contoh:

// Mendefinisikan komponen fungsi "NumberList" yang menerima props
function NumberList(props) {
  // Mengambil array numbers dari props dan membuat daftar elemen li dengan key unik
  const numbers = props.numbers;
  const listItems = numbers.map((number) =>
    <li key={number.toString()}>
      {number}
    </li>
  );

  // Mengembalikan elemen ul yang berisi daftar elemen li
  return (
    <ul>{listItems}</ul>
  );
}

// Array numbers yang akan dikirim sebagai props
const numbers = [1, 2, 3, 4, 5];

// Merender komponen "NumberList" dengan props numbers
ReactDOM.render(<NumberList numbers={numbers} />, document.getElementById('root'));