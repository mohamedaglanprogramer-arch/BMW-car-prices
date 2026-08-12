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


        /* =========================
           الصفحة الرئيسية
        ========================= */

        .container {
            min-height: 100vh;

            display: flex;

            justify-content: center;
            align-items: center;

            padding: 20px;
        }


        .content {
            width: 100%;
            max-width: 700px;

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

            text-shadow:
                0 3px 10px rgba(0, 0, 0, 0.5);
        }


        .content p {
            font-size: 22px;

            line-height: 1.8;

            color: #ffffff;
        }


        /* =========================
           زر اكتشف المزيد
        ========================= */

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

            box-shadow:
                0 5px 15px rgba(0, 0, 0, 0.25);
        }


        .btn:hover {
            background: #e4b74a;

            transform: translateY(-3px);

            box-shadow:
                0 8px 20px rgba(0, 0, 0, 0.3);
        }


        /* =========================
           نافذة الصورة
        ========================= */

        .image-popup {
            display: none;

            position: fixed;

            inset: 0;

            z-index: 9999;

            background: rgba(0, 0, 0, 0.88);

            justify-content: center;

            align-items: center;

            padding: 20px;

            overflow-y: auto;
        }


        /* =========================
           محتوى النافذة
        ========================= */

        .popup-content {
            display: flex;

            flex-direction: column;

            align-items: center;

            text-align: center;

            width: 100%;

            max-width: 600px;

            padding: 20px 0;
        }


        /* =========================
           الصورة
        ========================= */

        .image-popup img {
            width: auto;

            max-width: 90%;

            max-height: 55vh;

            object-fit: contain;

            border-radius: 20px;

            box-shadow:
                0 0 40px rgba(0, 0, 0, 0.6);

            animation: zoom 0.4s ease;
        }


        /* =========================
           الكلام تحت الصورة
        ========================= */

        .popup-text {
            width: 100%;

            margin-top: 20px;

            color: white;

            animation: textShow 0.6s ease;
        }


        .popup-text h1 {
            color: #f6c453;

            font-size: 32px;

            margin-bottom: 18px;

            text-shadow:
                0 3px 10px rgba(0, 0, 0, 0.6);
        }


        /* =========================
           كارت معلومات المنتج
        ========================= */

        .product-info {
            width: 100%;

            max-width: 500px;

            margin: auto;

            padding: 18px;

            background: rgba(255, 255, 255, 0.08);

            border: 1px solid rgba(246, 196, 83, 0.35);

            border-radius: 20px;

            backdrop-filter: blur(8px);

            -webkit-backdrop-filter: blur(8px);

            box-shadow:
                0 10px 30px rgba(0, 0, 0, 0.4);
        }


        /* =========================
           عناصر المعلومات
        ========================= */

        .info-item {
            display: flex;

            align-items: center;

            gap: 12px;

            text-align: right;

            padding: 14px 8px;

            color: #ffffff;

            font-size: 19px;

            border-bottom:
                1px solid rgba(255, 255, 255, 0.12);
        }


        .info-item:last-of-type {
            border-bottom: none;
        }


        /* =========================
           أيقونات المعلومات
        ========================= */

        .info-item .icon {
            width: 42px;

            height: 42px;

            min-width: 42px;

            display: flex;

            align-items: center;

            justify-content: center;

            background:
                rgba(201, 149, 46, 0.2);

            border:
                1px solid rgba(246, 196, 83, 0.25);

            border-radius: 50%;

            font-size: 20px;
        }


        .info-item strong {
            color: #f6c453;
        }


        /* =========================
           السعر
        ========================= */

        .price-box {
            margin-top: 18px;

            padding: 15px 20px;

            display: flex;

            justify-content: space-between;

            align-items: center;

            background:
                linear-gradient(
                    135deg,
                    #a87316,
                    #e4b74a
                );

            border-radius: 15px;

            color: white;

            box-shadow:
                0 7px 20px rgba(0, 0, 0, 0.35);

            border:
                1px solid rgba(255, 255, 255, 0.2);
        }


        .price-box span {
            font-size: 20px;

            font-weight: bold;
        }


        .price-box strong {
            font-size: 30px;

            color: #ffffff;

            text-shadow:
                0 2px 5px rgba(0, 0, 0, 0.3);
        }


        /* =========================
           جملة أسفل المعلومات
        ========================= */

        .product-note {
            margin-top: 18px;

            color: #f6c453;

            font-size: 17px;

            line-height: 1.7;

            font-weight: bold;
        }


        /* =========================
           زر الإغلاق
        ========================= */

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

            z-index: 10000;

            box-shadow:
                0 5px 20px rgba(0, 0, 0, 0.5);

            transition: 0.3s;
        }


        .close:hover {
            background: #e4b74a;

            transform: rotate(90deg);
        }


        /* =========================
           حركة الصورة
        ========================= */

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


        /* =========================
           حركة الكلام
        ========================= */

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


        /* =========================
           الموبايل
        ========================= */

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

                padding-top: 35px;
            }


            .image-popup img {
                max-width: 95%;

                max-height: 45vh;

                border-radius: 15px;
            }


            .popup-text h1 {
                font-size: 25px;

                margin-bottom: 15px;
            }


            .product-info {
                padding: 12px;

                border-radius: 16px;
            }


            .info-item {
                font-size: 16px;

                padding: 11px 5px;

                gap: 9px;
            }


            .info-item .icon {
                width: 35px;

                height: 35px;

                min-width: 35px;

                font-size: 17px;
            }


            .price-box {
                padding: 13px 15px;
            }


            .price-box span {
                font-size: 18px;
            }


            .price-box strong {
                font-size: 25px;
            }


            .product-note {
                font-size: 14px;

                margin-top: 15px;
            }


            .close {
                top: 15px;

                right: 15px;

                width: 45px;

                height: 45px;

                font-size: 27px;
            }
        }

    </style>

</head>


<body>


    <!-- =========================
         الصفحة الرئيسية
    ========================== -->

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

            <a
                class="btn"
                onclick="openImage()"
            >
                اكتشف المزيد
            </a>

        </div>

    </div>



    <!-- =========================
         نافذة المنتج
    ========================== -->

    <div
        class="image-popup"
        id="imagePopup"
    >


        <!-- زر الإغلاق -->

        <button
            class="close"
            onclick="closeImage()"
        >
            ×
        </button>



        <!-- محتوى النافذة -->

        <div class="popup-content">


            <!-- صورة المنتج -->

            <img
                src="https://chatgpt.com/backend-api/estuary/public_content/enc/eyJpZCI6Im1fNmE3YjM0YTNiM2M0ODE5MWIwMzUxYzE4YmEzNDI5OTk6ZmlsZV8wMDAwMDAwMDMyN2M4MWY0ODhhY2U2YzczY2VmMWFjMSIsImdpem1vX2lkIjpudWxsLCJ3aWQiOm51bGwsIm9pZCI6bnVsbCwic2lkIjpudWxsLCJjcyI6bnVsbCwiZm4iOm51bGwsImNkIjpudWxsLCJ0cyI6IjIwNjc2IiwicCI6InB5aSIsImNpZCI6IjEiLCJzaWciOiIwZjdlNTQzNzVmNzE0NzliZmJiNTU5YWVlNDIzZDU3MzczYzgzMmI2MzliNWI5NjZjY2FiZmU2NjBkNDkzNWY4IiwidiI6IjAiLCJjZG4iOm51bGwsImNwIjpudWxsLCJtYSI6bnVsbH0="
                alt="بلح آل عجلان"
            >



            <!-- معلومات المنتج -->

            <div class="popup-text">


                <h1>
                    🌴 بلح العجلان
                </h1>


                <div class="product-info">


                    <div class="info-item">

                        <span class="icon">
                            ⭐
                        </span>

                        <span>
                            أجود أنواع البلح
                        </span>

                    </div>



                    <div class="info-item">

                        <span class="icon">
                            ⚖️
                        </span>

                        <span>
                            الوزن:
                            <strong>5 كيلو</strong>
                        </span>

                    </div>



                    <div class="info-item">

                        <span class="icon">
                            📍
                        </span>

                        <span>
                            النوع:
                            <strong>الوادي والواحات</strong>
                        </span>

                    </div>

                    <div class="info-item">
                        <span class="icon">
                            📱
                        </span>
                        <span>
                            الرقم:
                            <strong><a>01141013558</a></strong>
                        </span>
                    </div>



                    <!-- السعر -->

                    <div class="price-box">

                        <span>
                            💰 السعر
                        </span>

                        <strong>
                            300 ج
                        </strong>

                    </div>


                </div>



                <!-- جملة جذابة -->

                <p class="product-note">

                    🌴 طعم طبيعي
                    •
                    جودة ممتازة
                    •
                    حلاوة لا تُقاوم

                </p>


            </div>


        </div>

    </div>



    <!-- =========================
         JavaScript
    ========================== -->

    <script>


        // فتح نافذة المنتج

        function openImage() {

            document.getElementById("imagePopup").style.display = "flex";

        }



        // إغلاق نافذة المنتج

        function closeImage() {

            document.getElementById("imagePopup").style.display = "none";

        }



        // إغلاق النافذة عند الضغط خارج المحتوى

        document
            .getElementById("imagePopup")
            .addEventListener("click", function(event) {

                if (event.target === this) {

                    closeImage();

                }

            });



        // إغلاق النافذة بزر ESC

        document.addEventListener("keydown", function(event) {

            if (event.key === "Escape") {

                closeImage();

            }

        });


    </script>


</body>

</html>
