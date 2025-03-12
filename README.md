# star-trail-effect
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Star Trail Effect</title>
    <style>
        body {
            margin: 0;
            overflow: hidden;
            background-color: black;
        }
        .star {
            position: absolute;
            width: 8px;
            height: 8px;
            background-color: white;
            border-radius: 50%;
            box-shadow: 0 0 10px white;
            animation: fadeOut 0.5s ease-out forwards;
        }
        @keyframes fadeOut {
            to {
                opacity: 0;
                transform: scale(2);
            }
        }
    </style>
</head>
<body>
    <script>
        document.addEventListener("mousemove", function (e) {
            const star = document.createElement("div");
            star.classList.add("star");
            document.body.appendChild(star);

            star.style.left = `${e.clientX}px`;
            star.style.top = `${e.clientY}px`;

            setTimeout(() => {
                star.remove();
            }, 500); // Star disappears after 0.5 seconds
        });
    </script>
</body>
</html>

