```html
<!DOCTYPE html>
<html lang="ar" dir="rtl">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">

    <title>بلح آل عجلان</title>

    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        html,
        body {
            width: 100%;
            min-height: 100%;
        }

        body {
            font-family: Arial, Tahoma, sans-serif;
            background-color: #120b05;

            background-image:
                linear-gradient(
                    rgba(0, 0, 0, 0.35),
                    rgba(0, 0, 0, 0.35)
                ),
                url("https://png.pngtree.com/background/20250122/original/pngtree-dates-sweet-food-islamic-holidays-decoration-ramadan-kareem-eid-mubarak-background-picture-image_16233606.jpg");

            background-size: cover;
            background-position: center;
            background-repeat: no-repeat;
            background-attachment: fixed;

            min-height: 100vh;
        }

        .container {
            min-height: 100vh;

            display: flex;
            justify-content: center;
            align-items: center;

            padding: 20px;
        }

        .content {
            text-align: center;
            color: white;

            background: rgba(0, 0, 0, 0.35);

            backdrop-filter: blur(4px);
            -webkit-backdrop-filter: blur(4px);

            padding: 40px;

            border-radius: 20px;

            border: 1px solid rgba(255, 255, 255, 0.15);

            box-shadow:
                0 15px 40px rgba(0, 0, 0, 0.4);
        }

        .content h1 {
            font-size: 50px;
            color: #f6c453;
            margin-bottom: 15px;
        }

        .content p {
            font-size: 22px;
            line-height: 1.8;
            color: #ffffff;
        }

        .btn {
            display: inline-block;

            margin-top: 25px;
            padding: 12px 30px;

            background: #c9952e;
            color: white;

            text-decoration: none;

            border-radius: 30px;

            font-size: 18px;
            font-weight: bold;

            cursor: pointer;

            transition: 0.3s;
        }

        .btn:hover {
            background: #e4b74a;

            transform: translateY(-3px);

            box-shadow:
                0 8px 20px rgba(0, 0, 0, 0.3);
        }

        /* نافذة الصورة */
        .image-popup {
            display: none;

            position: fixed;

            inset: 0;

            z-index: 9999;

            background: rgba(0, 0, 0, 0.85);

            justify-content: center;
            align-items: center;

            padding: 20px;
        }

        /* محتوى النافذة */
        .popup-content {
            display: flex;
            flex-direction: column;
            align-items: center;

            text-align: center;

            max-width: 90%;
        }

        /* الصورة */
        .image-popup img {
            max-width: 90%;
            max-height: 65vh;

            object-fit: contain;

            border-radius: 20px;

            border: none;

            box-shadow:
                0 0 40px rgba(0, 0, 0, 0.5);

            animation: zoom 0.4s ease;
        }

        /* الكلام تحت الصورة */
        .popup-text {
            margin-top: 20px;

            color: white;

            animation: textShow 0.6s ease;
        }

        .popup-text h2 {
            color: #fffffe;

            font-size: 30px;

            margin-bottom: 10px;
        }

        .popup-text p {
            color: white;

            font-size: 19px;

            line-height: 1.8;
        }

        /* زر الإغلاق */
        .close {
            position: absolute;

            top: 20px;
            right: 30px;

            width: 50px;
            height: 50px;

            border-radius: 50%;

            border: none;

            background: #c9952e;

            color: white;

            font-size: 30px;

            cursor: pointer;

            box-shadow:
                0 5px 20px rgba(0, 0, 0, 0.5);
        }

        .close:hover {
            background: #e4b74a;
        }

        /* حركة الصورة */
        @keyframes zoom {
            from {
                opacity: 0;
                transform: scale(0.7);
            }

            to {
                opacity: 1;
                transform: scale(1);
            }
        }

        /* حركة الكلام */
        @keyframes textShow {
            from {
                opacity: 0;
                transform: translateY(20px);
            }

            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        /* الموبايل */
        @media (max-width: 600px) {

            .content {
                width: 100%;
                padding: 30px 20px;
            }

            .content h1 {
                font-size: 35px;
            }

            .content p {
                font-size: 18px;
            }

            .popup-content {
                max-width: 95%;
            }

            .image-popup img {
                max-width: 95%;
                max-height: 60vh;
            }

            .popup-text h2 {
                font-size: 23px;
            }

            .popup-text p {
                font-size: 16px;
            }

            .close {
                top: 15px;
                right: 15px;
            }
        }
    </style>
</head>

<body>

    <div class="container">

        <div class="content">
          

            <h1>
                🌴 بلح آل عجلان 🫘
            </h1>

            <p>
                بلح طبيعي بمذاق غني وحلاوة لا تقاوم
                <br>
                طعم الطبيعة حلو في كل حبة 🌴
            </p>

            <a class="btn" onclick="openImage()">
                اكتشف المزيد
            </a>

        </div>

    </div>


    <!-- نافذة الصورة -->
    <div class="image-popup" id="imagePopup">

        <!-- زر الإغلاق -->
        <button class="close" onclick="closeImage()">
            ×
        </button>

        <!-- محتوى النافذة -->
        <div class="popup-content">

            <!-- الصورة -->
            <img
                src="https://chatgpt.com/backend-api/estuary/public_content/enc/eyJpZCI6Im1fNmE3YjM0YTNiM2M0ODE5MWIwMzUxYzE4YmEzNDI5OTk6ZmlsZV8wMDAwMDAwMDMyN2M4MWY0ODhhY2U2YzczY2VmMWFjMSIsImdpem1vX2lkIjpudWxsLCJ3aWQiOm51bGwsIm9pZCI6bnVsbCwic2lkIjpudWxsLCJjcyI6bnVsbCwiZm4iOm51bGwsImNkIjpudWxsLCJ0cyI6IjIwNjc2IiwicCI6InB5aSIsImNpZCI6IjEiLCJzaWciOiIwZjdlNTQzNzVmNzE0NzliZmJiNTU5YWVlNDIzZDU3MzczYzgzMmI2MzliNWI5NjZjY2FiZmU2NjBkNDkzNWY4IiwidiI6IjAiLCJjZG4iOm51bGwsImNwIjpudWxsLCJtYSI6bnVsbH0="
                alt="بلح آل عجلان">

            <!-- الكلام الذي يظهر تحت الصورة -->
            <div class="popup-text">

                <h1>
            بلح العجلان 5ك
                </h1>
                <br>
               <br>
 
             <h2> <ol type="I">

               <li>اجود انوع البلح    </li>
               <br>
               <li>الوزن : 5 كيلو      </li>
               <br>
               <li>النوع: الوادي ,الوحات</li>
               <br>
               <li>السعر:<b>300ج</b></li>
        
                </ol>

            </h2>
                > 
                
                  
                   
                  

            </div>

        </div>

    </div>


    <script>

        function openImage() {
            document.getElementById("imagePopup").style.display = "flex";
        }

        function closeImage() {
            document.getElementById("imagePopup").style.display = "none";
        }

        /* إغلاق النافذة عند الضغط خارج المحتوى */
        document.getElementById("imagePopup").addEventListener("click", function(event) {

            if (event.target === this) {
                closeImage();
            }

        });

    </script>

</body>

</html>
```
