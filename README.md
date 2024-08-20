<!DOCTYPE html>
<html>
<head>
    <title>Kelas Robot</title>
</head>
<body>
    <p>Waktu saat ini: WIB - <span id="wib"></span> | WITA - <span id="wita"></span> | WIT - <span id="wit"></span></p>

    <script>
        function updateTime() {
            const now = new Date();
            const options = { timeZone: 'Asia/Jakarta', hour: '2-digit', minute: '2-digit', second: '2-digit' };
            document.getElementById('wib').innerText = new Intl.DateTimeFormat('id-ID', options).format(now);

            options.timeZone = 'Asia/Makassar';
            document.getElementById('wita').innerText = new Intl.DateTimeFormat('id-ID', options).format(now);

            options.timeZone = 'Asia/Jayapura';
            document.getElementById('wit').innerText = new Intl.DateTimeFormat('id-ID', options).format(now);
        }
        setInterval(updateTime, 1000);
        updateTime();
    </script>
</body>
</html>
