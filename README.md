<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Spa">
    <title>Spa</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Montserrat', sans-serif;
            color: #2c2c2c;
            background-color: #f9f9f9;
            scroll-behavior: smooth;
        }

        #instagram{
            border-radius: 20px;
            background: linear-gradient(135deg, #f09433 0%, #e6683c 25%, #dc2743 50%, #cc2366 75%, #bc1888 100%);
            box-shadow: 0 4px 15px rgba(0, 0, 0, 0.2);
            color: white;
            padding: 15px;
            font-size: 30px;
            position: fixed;
            right: 10px;
            bottom: 10px;
        }

        #facebook{
            border-radius: 10px;
            background-color: #1877f2;
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
            padding: 15px;
            font-size: 30px;
            position: fixed;
            right: 10px;
            bottom: 10px;
        }

        .container {
            width: 85%;
            margin: auto;
        }

        /* Header */
        /* Header and Navbar */
        .header {
            background-color: #fff;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
            position: sticky;
            top: 0;
            z-index: 1000;
        }

        .navbar {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 20px 0;
        }

        .logo {
            font-family: 'Playfair Display', serif;
            font-size: 2.5rem;
            color: #037103;
        }

        .nav-links {
            display: flex;
            list-style: none;
            transition: transform 0.3s ease-in-out;
        }

        .nav-links li {
            margin-left: 30px;
        }

        .nav-links a {
            text-decoration: none;
            color: #2c2c2c;
            font-weight: 700;
        }

        .cta-button {
            background-color: #037103;
            color: white;
            padding: 10px 20px;
            border-radius: 30px;
            font-weight: 700;
        }

        #services_btn{
            transform: scale(0);
            animation: zoomIn 10s ease-out forwards;
        }

        @keyframes zoomIn {
            0% {
            transform: scale(0);
            opacity: 0;
            }
            60% {
            transform: scale(1);
            opacity: 1;
            }
            100% {
            transform: scale(1);
            }
        }

        .menu-toggle {
            display: none;
            font-size: 2rem;
            background: none;
            border: none;
            color: #2c2c2c;
            cursor: pointer;
        }

        /* Mobile View Styling */
        @media (max-width: 768px) {

            /* Hero */
            .hero {
                background-image: url('https://firebasestorage.googleapis.com/v0/b/digitalsignature-af550.appspot.com/o/newpics%2Fmobile_view_bg_image.jpeg?alt=media&token=a6f1fd1a-b09d-4a56-82b4-6174bbbb0b51');
                background-size: cover;
                background-position: center;
                height: 90vh;
                display: flex;
                justify-content: center;
                align-items: center;
                text-align: center;
                color: white;
            }

            #home h2 {
                font-size: 2.5rem;
            }

            #home p{
                font-size: 1.2rem;
            }

            .menu-toggle {
                display: block;
            }

            .nav-links {
                display: none;
                position: absolute;
                top: 100%;
                left: 0;
                width: 100%;
                background-color: #fff;
                flex-direction: column;
                align-items: center;
                box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1);
            }

            .nav-links.show {
                display: flex;
            }

            .nav-links li {
                margin: 15px 0;
            }

            .cta-button {
                margin-top: 15px;
            }

            .logo {
                font-size: 22px;
            }
            
        }

        @media (min-width: 768px) {
            .hero {
                background-image: url('https://firebasestorage.googleapis.com/v0/b/digitalsignature-af550.appspot.com/o/newpics%2Fbg_1.png?alt=media&token=24180952-1fcc-47d5-becb-b24beb9d4021');
                background-size: cover;
                background-position: center;
                height: 90vh;
                display: flex;
                justify-content: center;
                align-items: center;
                text-align: center;
                color: white;
            }
        }

        .nav-links a:hover {
            color: #037103;
        }

        a{
            text-decoration: none;
        }




        .hero h2 {
            font-family: 'Playfair Display', serif;
            font-size: 3rem;
            margin-bottom: 20px;
        }

        .hero p {
            font-size: 1.5rem;
            margin-bottom: 40px;
        }

        /* Services */
        .services {
            padding: 80px 0;
            background-color: #fff;
        }

        .section-title {
            font-family: 'Playfair Display', serif;
            font-size: 2.8rem;
            margin-bottom: 50px;
            text-align: center;
            color: #2c2c2c;
        }

        .services-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 30px;
        }

        .service-box {
            text-align: center;
            background-color: #f9f9f9;
            padding: 10px;
            border-radius: 15px;
            box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1);
            transition: transform 0.3s ease;
        }

        .service-box p {
            font-size: 1rem;
            color: #555;
        }

        .service-box:hover {
            color: #037103;
        }

        .service-box img{
            width: 300px;
            height: 300px;
        }

        .service-box h3 {
            font-family: 'Playfair Display', serif;
            font-size: 1.8rem;
            margin: 20px 0;
        }


        /* Gallery */
        .gallery {
            padding: 80px 0;
            background-color: #f9f9f9;
        }

        .gallery-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 30px;
        }

        .gallery-item img {
            width: 100%;
            height: 200px;
            border-radius: 15px;
            transition: transform 0.3s ease;
        }

        .gallery-item img:hover {
            transform: scale(1.05);
        }

        .gallery-item h3 {
            text-align: center;
            padding-top: 20px;
        }

        /* Reviews */
        .reviews {
            padding: 80px 0;
            background-color: #fff;
        }

        .review-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
        }

        .review-box {
            background-color: #f9f9f9;
            padding: 40px;
            border-radius: 15px;
            box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1);
            text-align: center;
        }

        .review-box p {
            font-size: 1.1rem;
            color: #333;
        }

        .review-box span {
            display: block;
            margin-top: 20px;
            font-weight: bold;
            color: #037103;
        }

        /* Contact */
        .contact {
            padding: 80px 0;
            text-align: center;
        }

        .contact p {
            font-size: 1.1rem;
        }

        /* Footer */
        .footer {
            background-color: #202020;
            color: white;
            padding: 20px 0;
            text-align: center;
        }

        .back-to-top {
            text-decoration: none;
            color: white;
            margin-top: 10px;
            display: block;
            font-size: 1rem;
        }

        body {
            -webkit-user-select: none; /* Disable text selection */
            -moz-user-select: none;
            -ms-user-select: none;
            user-select: none;
            -webkit-touch-callout: none; /* Disable long tap on mobile */
        }
        img {
            pointer-events: none; /* Disable image drag */
        }

    </style>
     <script src="https://kit.fontawesome.com/eccb15858b.js" crossorigin="anonymous"></script>
    <link href="https://fonts.googleapis.com/css2?family=Montserrat:wght@400;700&family=Playfair+Display:wght@600&display=swap" rel="stylesheet">
</head>
<body>
    <header class="header">
        <div class="container">
            <nav class="navbar">
                <button class="menu-toggle" aria-label="Toggle Menu">☰</button>
                <div class="logo-container">
                    <h1 class="logo">The Spas</h1>
                </div>
                <ul class="nav-links">
                    <li><a href="#home">Home</a></li>
                    <li><a href="#services">Our Services</a></li>
                    <li><a href="#gallery">Gallery</a></li>
                    <li><a href="#reviews">Reviews</a></li>
                    <li><a href="#contact">Contact</a></li>
                </ul>
                <a href="tel:6374145755" class="cta-button">Call</a>
            </nav>
        </div>
    </header>

    <a id="instagram" href="https://www.instagram.com/thespas.india/">
      <i class="fa-brands fa-instagram"></i>
    </a>




    <section id="home" class="hero">
        <div class="hero-content">
            <h2 id="header_text">Your Luxury Spa Experience Awaits</h2>
            <p id="header_sub_text">Indulge in the finest treatments and the ultimate relaxation at our Spa. Let us pamper you.</p>
            <a href="#services" id="services_btn" class="cta-button">Explore Our Services</a>
        </div>
    </section>

    <section id="services" class="services">
        <div class="container">
            <h2 class="section-title">Our Premium Services</h2>
            <div class="services-grid">
                <div class="service-box">
                    <img src="https://firebasestorage.googleapis.com/v0/b/digitalsignature-af550.appspot.com/o/newpics%2Fclassic_massage.jpeg?alt=media&token=79680bd5-62ab-42fb-ac08-679cb03f4271" alt="Nail Treatment">
                    <h3>Classic Massage</h3>
                    <p>Relax and rejuvenate with our classic massage, easing tension and enhancing wellness.</p>
                </div>
                <div class="service-box">
                    <img src="https://firebasestorage.googleapis.com/v0/b/digitalsignature-af550.appspot.com/o/newpics%2Fpremium_massage.jpeg?alt=media&token=f18bc152-d385-4300-8e63-9833aa47026d" alt="Spa Treatment">
                    <h3>Premium Massage</h3>
                    <p>Experience ultimate relaxation with our premium massage, tailored for luxurious rejuvenation and comfort.</p>
                </div>
                <div class="service-box">
                    <img src="https://firebasestorage.googleapis.com/v0/b/digitalsignature-af550.appspot.com/o/parlour_services_img%2Ftraditional_massage_pic.jpg?alt=media&token=6ae81d67-2bf4-460b-89f2-335782637ba1" alt="Massage">
                    <h3>Traditional Massage</h3>
                    <p>Reconnect with timeless techniques in our traditional massage, promoting balance and deep relaxation.</p>
                </div>
                <div class="service-box">
                    <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcRWcoVdIR9Q-Yd5XALZZKWutwBndhSbQKnM4A&s" alt="Facial">
                    <h3>Swedish Massage</h3>
                    <p>Unwind with our Swedish massage, relieving stress and boosting circulation for ultimate relaxation.</p>
                </div>
                <div class="service-box">
                    <img src="https://firebasestorage.googleapis.com/v0/b/digitalsignature-af550.appspot.com/o/newpics%2Fdeep_tissue_massage.jpeg?alt=media&token=dcf5fc8f-bc1e-4bc5-995b-4db3046724cf" alt="Nail Treatment">
                    <h3>Deep Tissue Massage</h3>
                    <p>Relieve chronic tension with our deep tissue massage, targeting deep layers for relaxation.</p>
                </div>
                <div class="service-box">
                    <img src="https://firebasestorage.googleapis.com/v0/b/digitalsignature-af550.appspot.com/o/newpics%2Fbg_1.png?alt=media&token=24180952-1fcc-47d5-becb-b24beb9d4021" alt="Spa Treatment">
                    <h3>Aromatherapy Massage</h3>
                    <p>Soothe your senses with our aromatherapy massage, blending essential oils for relaxation.</p>
                </div>
                <div class="service-box">
                    <img src="https://firebasestorage.googleapis.com/v0/b/digitalsignature-af550.appspot.com/o/parlour_services_img%2Ftrigger_point_massage_pic.jpg?alt=media&token=317e788d-d711-4ce5-9445-c449ac37b330" alt="Massage">
                    <h3>Triger Point Massage</h3>
                    <p>Ease pain and tension with our trigger point massage, targeting specific muscle knots.</p>
                </div>
                <div class="service-box">
                    <img src="https://firebasestorage.googleapis.com/v0/b/digitalsignature-af550.appspot.com/o/newpics%2Fhot_stone_massage.jpeg?alt=media&token=fbd2ab61-3195-44ab-84f2-ec5e7a269bb5" alt="Facial">
                    <h3>Hot Stone Massage</h3>
                    <p>Experience deep relaxation with our hot stone massage, easing tension and restoring balance.</p>
                </div>
                <div class="service-box">
                    <img src="https://firebasestorage.googleapis.com/v0/b/digitalsignature-af550.appspot.com/o/newpics%2F2.jpg?alt=media&token=ca8cf20f-7b7f-43ba-8489-28cef87567ef" alt="Nail Treatment">
                    <h3>Relaxation Massage</h3>
                    <p>Melt away stress with our relaxation massage, promoting calmness and overall well-being.</p>
                </div>
                <div class="service-box">
                    <img src="https://firebasestorage.googleapis.com/v0/b/digitalsignature-af550.appspot.com/o/parlour_services_img%2Fcouple_massage_pic.jpg?alt=media&token=e5a7f551-0f70-4d2e-adf5-2d3cca57e267" alt="Spa Treatment">
                    <h3>Couple Massage</h3>
                    <p>Enjoy a shared experience with our couple massage, offering relaxation and bonding in harmony.</p>
                </div>
                <div class="service-box">
                    <img src="https://firebasestorage.googleapis.com/v0/b/digitalsignature-af550.appspot.com/o/parlour_services_img%2Fleg_fatigue_release_massge_pic.jpg?alt=media&token=1e8bbbd4-e300-46d7-b2cb-6a158b1280ab" alt="Massage">
                    <h3>Leg Fatigue Releiver Massage</h3>
                    <p>Revitalize tired legs with our leg fatigue reliever massage, boosting circulation and soothing muscles.</p>
                </div>
                <div class="service-box">
                    <img src="https://firebasestorage.googleapis.com/v0/b/digitalsignature-af550.appspot.com/o/parlour_services_img%2Fhead_foot_massage_pic.jpg?alt=media&token=887e6971-040b-4cec-bccd-e7b8c45a74a9" alt="Facial">
                    <h3>Head & Foot Masage</h3>
                    <p>Relax and rejuvenate with our head and foot massage, relieving tension and promoting calm.</p>
                </div>
            </div>
        </div>
    </section>

    <section id="gallery" class="gallery">
        <div class="container">
            <h2 class="section-title">Our Promises</h2>
            <div class="gallery-grid">
                <div class="gallery-item"><img src="https://firebasestorage.googleapis.com/v0/b/digitalsignature-af550.appspot.com/o/parlour_our_work_img%2Fquality_service.jpg?alt=media&token=7a572c8b-1bd0-4df3-a622-47b0cb94bc96" alt=""><h3>Certified Expereinced Therapist</h3></div>
                <div class="gallery-item"><img src="https://firebasestorage.googleapis.com/v0/b/digitalsignature-af550.appspot.com/o/parlour_our_work_img%2Four_work_2.jpg?alt=media&token=6570e856-63e0-41d6-a442-b5b9a63c87bd" alt=""><h3>Commitment to Hygienic</h3></div>
                <div class="gallery-item"><img src="https://firebasestorage.googleapis.com/v0/b/digitalsignature-af550.appspot.com/o/parlour_our_work_img%2Four_work_4.jpg?alt=media&token=bdbaaf71-e3f7-4dda-a314-cdc8ad00817e" alt=""><h3>Quality Services</h3></div>
                <div class="gallery-item"><img src="https://firebasestorage.googleapis.com/v0/b/digitalsignature-af550.appspot.com/o/parlour_our_work_img%2Fhigh_quality_Product.jpg?alt=media&token=7fd5d494-a500-4be7-b9bc-2506c0bcbca0" alt=""><h3>Use of High Quality Products</h3></div>
            </div>
        </div>
    </section>

    <section id="reviews" class="reviews">
        <div class="container">
            <h2 class="section-title">What Our Clients Say</h2>
            <div class="review-grid">
                <div class="review-box">
                    <p>"The best nail and spa experience I've ever had! The team is so professional, and the atmosphere is so calming. Highly recommend!"</p>
                    <span>- Lakshmi.</span>
                </div>
                <div class="review-box">
                    <p>"This spa exceeded all my expectations! I left feeling completely rejuvenated. Can't wait for my next visit!"</p>
                    <span>- Shruthi.</span>
                </div>
                <div class="review-box">
                    <p>"Amazing service and gorgeous results. The spa is beautifully designed, and the staff makes you feel so pampered!"</p>
                    <span>- Swetha.</span>
                </div>
            </div>
        </div>
    </section>

    <section id="contact" class="contact">
        <div class="container">
            <h2 class="section-title">Get in Touch</h2>
            <p>We'd love to hear from you! Visit us at No:122, Canteen St, Behind Axis Bank, Puducherry-605001, or contact us at:</p>
            <p>Email: mailme.thespa@gmail.com | Phone: 6374145755</p>
        </div>
    </section>

    <footer class="footer">
        <div class="container">
            <p>&copy; 2024 The Spas. All Rights Reserved.</p>
            <a href="#home" class="back-to-top">Back to Top</a>
            <br>
        </div>
    </footer>
<script>
    document.getElementById("header_text").innerHTML = ""
document.getElementById("header_sub_text").innerHTML = ""
document.addEventListener('DOMContentLoaded', () => {
    const menuToggle = document.querySelector('.menu-toggle');
    const navLinks = document.querySelector('.nav-links');

    menuToggle.addEventListener('click', () => {
        navLinks.classList.toggle('show');
    });
});

function descriptionSubHeader(textContent){
    let dhi = 0;
    let dhtxt = textContent;
    let dhtxtArr =dhtxt.split(""); 
    let dhspeed = 50;
    let dhtemp=" ";
    function descriptionSubHeaderWrite(){
        if (dhi < dhtxt.length) {
        document.getElementById("header_sub_text").innerText = dhtemp + dhtxtArr[dhi]+ "|";
        dhtemp = dhtemp + dhtxtArr[dhi];
        dhi++;
        setTimeout(descriptionSubHeaderWrite, dhspeed);
        }else{
        document.getElementById("header_sub_text").innerHTML = textContent;
        
        }
    }
    descriptionSubHeaderWrite();
    }


function descriptionHeader(textContent){
    let dhi = 0;
    let dhtxt = textContent;
    let dhtxtArr =dhtxt.split(""); 
    let dhspeed = 50;
    let dhtemp=" ";
    function descriptionHeaderWrite(){
        if (dhi < dhtxt.length) {
        document.getElementById("header_text").innerText = dhtemp + dhtxtArr[dhi]+ "|";
        dhtemp = dhtemp + dhtxtArr[dhi];
        dhi++;
        setTimeout(descriptionHeaderWrite, dhspeed);
        }else{
        document.getElementById("header_text").innerHTML = textContent;
        descriptionSubHeader("Indulge in the finest treatments and the ultimate relaxation at our Spa. Let us pamper you.")
        }
    }
    descriptionHeaderWrite();
    }

    descriptionHeader("Your Luxury Spa Experience Awaits")


    let devtools = false;
  setInterval(function() {
    const widthThreshold = window.outerWidth - window.innerWidth > 100;
    const heightThreshold = window.outerHeight - window.innerHeight > 100;
    if (widthThreshold || heightThreshold) {
      devtools = true;
      alert('Developer tools are disabled on this site.');
      window.location.reload();
    }
  }, 500);

  document.addEventListener('keydown', function(e) {
    // Disable F12
    if (e.keyCode === 123) {
      e.preventDefault();
    }
    // Disable Ctrl+Shift+I, Ctrl+Shift+J, Ctrl+U
    if (e.ctrlKey && (e.keyCode === 73 || e.keyCode === 74 || e.keyCode === 85 || e.keyCode === 83)) {
      e.preventDefault();
    }
  });

  document.addEventListener('contextmenu', function(e) {
    e.preventDefault();
  });
</script>
</body>
</html>
