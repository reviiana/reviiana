- osis_registration/
  - index.html
  - styles.css
  - script.js
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Pendaftaran OSIS</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <div class="container">
        <h1>Pendaftaran OSIS</h1>

        <form id="registrationForm">
            <label for="name">Nama Lengkap:</label>
            <input type="text" id="name" name="name" required>

            <label for="class">Kelas:</label>
            <select id="class" name="class" required>
                <option value="10">Kelas 10</option>
                <option value="11">Kelas 11</option>
                <option value="12">Kelas 12</option>
            </select>

            <label for="position">Jabatan yang diinginkan:</label>
            <select id="position" name="position" required>
                <option value="Ketua">Ketua</option>
                <option value="Wakil Ketua">Wakil Ketua</option>
                <option value="Sekretaris">Sekretaris</option>
                <option value="Bendahara">Bendahara</option>
                <option value="Seksi Acara">Seksi Acara</option>
                <option value="Seksi Dokumentasi">Seksi Dokumentasi</option>
            </select>

            <button type="submit">Daftar</button>
        </form>

        <div id="schedule">
            <h2>Informasi Jadwal</h2>
            <p><strong>Program Kerja:</strong></p>
            <ul id="programList">
                <li>1 Januari: Rapat Program Kerja</li>
                <li>14 Februari: Lomba Kebersihan</li>
                <li>21 Maret: Seminar Pendidikan</li>
            </ul>
            <p><strong>Jadwal Piket:</strong></p>
            <ul id="piketList">
                <li>Senin: Kelas 10A</li>
                <li>Selasa: Kelas 10B</li>
                <li>Rabu: Kelas 11A</li>
                <li>Kamis: Kelas 11B</li>
                <li>Jumat: Kelas 12A</li>
            </ul>
        </div>
    </div>

    <script src="script.js"></script>
</body>
</html>
body {
    font-family: Arial, sans-serif;
    background-color: #f4f4f4;
    margin: 0;
    padding: 0;
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100vh;
}

.container {
    background-color: white;
    padding: 20px;
    border-radius: 10px;
    box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
    width: 300px;
}

h1, h2 {
    text-align: center;
    color: #333;
}

form {
    display: flex;
    flex-direction: column;
}

label {
    margin-top: 10px;
    margin-bottom: 5px;
    color: #555;
}

input, select {
    padding: 8px;
    border: 1px solid #ccc;
    border-radius: 5px;
    margin-bottom: 10px;
}

button {
    padding: 10px;
    background-color: #5cb85c;
    color: white;
    border: none;
    border-radius: 5px;
    cursor: pointer;
}

button:hover {
    background-color: #4cae4c;
}

#schedule {
    margin-top: 20px;
}

ul {
    list-style-type: none;
    padding: 0;
}
document.getElementById("registrationForm").addEventListener("submit", function(event){
    event.preventDefault();

    let name = document.getElementById("name").value;
    let kelas = document.getElementById("class").value;
    let position = document.getElementById("position").value;

    alert(`Terima kasih, ${name}!\nAnda telah mendaftar untuk kelas ${kelas} dengan jabatan ${position}.`);
});
