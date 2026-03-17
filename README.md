# Elevation-Sabbath-
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Elevation Sabbath 2026</title>
    <link href="https://fonts.googleapis.com/css2?family=Playfair+Display:ital,wght@0,400;0,700;0,900;1,400&family=Cinzel:wght@400;700&display=swap" rel="stylesheet">
    <style>
        :root {
            --burgundy: #6B1A2A; --deep-burgundy: #3A0A15; --gold: #C9922A;
            --light-gold: #E8B84B; --cream: #F7F0E6; --charcoal: #120508;
        }
        * { box-sizing: border-box; margin: 0; padding: 0; }
        body {
            background: var(--charcoal);
            display: flex; flex-direction: column; align-items: center;
            min-height: 100vh; padding: 40px 20px;
            font-family: 'Playfair Display', serif;
        }
        /* The Flyer Card */
        .flyer {
            width: 100%; max-width: 450px;
            background: var(--deep-burgundy);
            position: relative; border: 1px solid rgba(201,146,42,0.3);
            box-shadow: 0 20px 50px rgba(0,0,0,0.6);
            padding: 40px 20px; text-align: center;
            overflow: hidden;
        }
        .frame { position: absolute; inset: 10px; border: 1px solid rgba(201,146,42,0.4); pointer-events: none; }
        .badge { font-family: 'Cinzel'; font-size: 10px; color: var(--gold); letter-spacing: 4px; text-transform: uppercase; margin-bottom: 15px; }
        h1 { font-size: 48px; color: var(--cream); line-height: 0.9; margin-bottom: 20px; }
        h1 span { display: block; font-style: italic; font-size: 38px; color: var(--light-gold); font-weight: 400; }
        
        .photo-container {
            width: 200px; height: 230px; margin: 0 auto 25px;
            border: 2px solid var(--gold); padding: 5px; background: rgba(0,0,0,0.2);
        }
        .photo-img { width: 100%; height: 100%; object-fit: cover; display: block; }

        .details-grid {
            display: grid; grid-template-columns: 1fr 1fr;
            gap: 20px; margin: 25px 0; padding: 20px;
            background: rgba(0,0,0,0.3); border-top: 1px solid rgba(201,146,42,0.2);
        }
        .label { font-family: 'Cinzel'; font-size: 9px; color: var(--gold); margin-bottom: 5px; }
        .value { color: var(--cream); font-size: 18px; font-weight: 700; }

        .scripture { font-style: italic; color: rgba(247,240,230,0.7); font-size: 14px; margin-top: 10px; line-height: 1.6; }

        /* Interactive Buttons */
        .controls { display: flex; flex-direction: column; gap: 12px; width: 100%; max-width: 450px; margin-top: 30px; }
        .btn {
            padding: 16px; border-radius: 4px; text-align: center;
            text-decoration: none; font-family: 'Cinzel'; font-weight: 700;
            font-size: 12px; transition: 0.3s; cursor: pointer; border: none;
        }
        .btn-download { background: var(--gold); color: var(--deep-burgundy); }
        .btn-whatsapp { background: #25D366; color: white; }
        .btn-map { background: transparent; border: 1px solid var(--gold); color: var(--gold); }
    </style>
</head>
<body>

    <div id="invite-card" class="flyer">
        <div class="frame"></div>
        <div class="badge">You are Invited</div>
        <h1>Elevation <span>Sabbath</span></h1>
        
        <div class="photo-container">
            <img src="https://inline-images.googleusercontent.com/AICcyfom0YwO3Y_8D3iZ3-O_pS_I3GfF6Y0_Q-M9i6_R" class="photo-img" alt="Minister">
        </div>

        <div class="details-grid">
            <div>
                <div class="label">Date</div>
                <div class="value">4 April 2026</div>
            </div>
            <div>
                <div class="label">Venue</div>
                <div class="value">Pimville Cathedral</div>
            </div>
        </div>

        <p class="scripture">"Those who hope in the Lord will renew their strength. They will soar on wings like eagles." <br>— Isaiah 40:31</p>
    </div>

    <div class="controls">
        <button class="btn btn-download" onclick="downloadInvite()">Download Image for Gallery</button>
        <a href="https://wa.me/?text=I%20am%20confirmed%20for%20Elevation%20Sabbath%20on%20April%204th!" class="btn btn-whatsapp" target="_blank">RSVP via WhatsApp</a>
        <a href="https://www.google.com/maps/search/Pimville+Cathedral" class="btn btn-map" target="_blank">View Location Map</a>
    </div>

    <script src="https://cdnjs.cloudflare.com/ajax/libs/html2canvas/1.4.1/html2canvas.min.js"></script>
    <script>
        function downloadInvite() {
            const invite = document.getElementById('invite-card');
            html2canvas(invite, { scale: 3 }).then(canvas => {
                const link = document.createElement('a');
                link.download = 'Elevation-Sabbath-Invite.png';
                link.href = canvas.toDataURL("image/png");
                link.click();
            });
        }
    </script>

</body>
</html>
