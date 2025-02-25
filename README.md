# satdirection
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Enter Your Registration Number</title>
    <style>
        /* Ảnh nền mặc định cho PC */
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            background: url('https://drive.google.com/uc?id=1BT9gsR2xJWUrURBxKkMVFfZJnjCJQW58') no-repeat center center;
            background-size: cover;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
        }

        /* Khi màn hình nhỏ hơn 768px (Mobile), đổi ảnh nền */
        @media (max-width: 768px) {
            body {
                background: url('https://drive.google.com/uc?id=1YyS1v5slIaVxEa6bDH5_SlYfQEewuc-I') no-repeat center center;
                background-size: cover;
            }
        }

        /* Container của ô nhập số */
        .container {
            background: rgba(255, 255, 255, 0.9);
            padding: 30px;
            border-radius: 12px;
            box-shadow: 0px 0px 15px rgba(0, 0, 0, 0.2);
            text-align: center;
            max-width: 400px;
            width: 90%;
        }

        /* Tiêu đề */
        h2 {
            font-size: 24px;
            margin-bottom: 20px;
        }

        /* Ô nhập số */
        input {
            width: 100%;
            padding: 15px;
            font-size: 20px;
            border: 2px solid #ccc;
            border-radius: 8px;
            text-align: center;
            outline: none;
        }

        /* Nút bấm */
        button {
            width: 100%;
            margin-top: 15px;
            background: #007bff;
            color: white;
            padding: 15px;
            border: none;
            border-radius: 8px;
            cursor: pointer;
            font-size: 18px;
            font-weight: bold;
        }

        button:hover {
            background: #0056b3;
        }
    </style>
    <script>
        function checkSBD() {
            var sbd = document.getElementById("sbd").value.trim();
            var roomLinks = {
                "1001": "https://sites.google.com/view/ttpnd1r1/trang-ch%E1%BB%A7",
                "1002": "https://sites.google.com/view/ttpnd1r1/trang-ch%E1%BB%A7",
                "1003": "https://example.com/phong3"
            };

            if (roomLinks[sbd]) {
                window.location.href = roomLinks[sbd]; 
            } else {
                alert("Your registration number is invalid");
            }
        }
    </script>
</head>
<body>

    <div class="container">
        <h2>Enter Your Registration Number</h2>
        <input type="text" id="sbd" placeholder="Enter your number" maxlength="10" 
               oninput="this.value = this.value.replace(/[^0-9]/g, '')">
        <button onclick="checkSBD()">Submit</button>
    </div>

</body>
</html>
