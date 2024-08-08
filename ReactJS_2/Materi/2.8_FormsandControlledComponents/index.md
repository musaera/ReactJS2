Pengertian:
Di React, form elements seperti <input>, <textarea>, dan <select> dikelola sebagai controlled components, di mana state elemen tersebut disimpan dalam state React dan diubah melalui event handler.
Contoh:

// Mengimpor React dan useState hook
import React, { useState } from 'react';

function NameForm() {
  // Mendefinisikan state "value" dengan nilai awal kosong
  const [value, setValue] = useState('');

  // Fungsi untuk menangani perubahan input dan mengupdate state "value"
  const handleChange = (event) => {
    setValue(event.target.value);
  }

  // Fungsi untuk menangani submit form dan menampilkan alert
  const handleSubmit = (event) => {
    alert('Nama yang diinput: ' + value);
    event.preventDefault(); // Mencegah default action dari form submit
  }

  // Mengembalikan form dengan input yang dikendalikan oleh state "value"
  return (
    <form onSubmit={handleSubmit}>
      <label>
        Nama:
        <input type="text" value={value} onChange={handleChange} />
      </label>
      <button type="submit">Submit</button>
    </form>
  );
}

// Merender komponen "NameForm" ke dalam elemen dengan id "root"
ReactDOM.render(<NameForm />, document.getElementById('root'));