# andrea
Task 4 of Intro to Digital by Hack Your Future
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Susan's Birthday Party</title>
    <link rel="icon" href="data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAxMDAgMTAwIj48dGV4dCB5PSIuOWVtIiBmb250LXNpemU9IjkwIj7wn46mPC90ZXh0Pjwvc3ZnPg==">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background: linear-gradient(135deg, #fffbf7 0%, #f5f1ed 100%);
            color: #1a1a1a;
            line-height: 1.6;
            min-height: 100vh;
            padding: 20px;
        }

        .container {
            max-width: 600px;
            margin: 0 auto;
            background: #fffbf7;
            border-radius: 12px;
            box-shadow: 0 8px 32px rgba(26, 26, 26, 0.1);
            padding: 50px 30px;
            animation: slideIn 0.6s ease-out;
        }

        @keyframes slideIn {
            from {
                opacity: 0;
                transform: translateY(20px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        .header {
            text-align: center;
            margin-bottom: 40px;
        }

        .emoji {
            font-size: 60px;
            margin-bottom: 15px;
            display: block;
        }

        h1 {
            font-family: 'Georgia', serif;
            font-size: 2.5em;
            color: #1a1a1a;
            margin-bottom: 10px;
            font-weight: 700;
        }

        .subtitle {
            font-size: 1.2em;
            color: #666;
            font-style: italic;
            margin-bottom: 30px;
        }

        .details {
            background: linear-gradient(135deg, rgba(196, 167, 71, 0.1) 0%, rgba(26, 26, 26, 0.03) 100%);
            padding: 25px;
            border-radius: 8px;
            margin-bottom: 30px;
            border-left: 4px solid #c4a747;
        }

        .detail-item {
            margin-bottom: 18px;
            display: flex;
            align-items: flex-start;
        }

        .detail-item:last-child {
            margin-bottom: 0;
        }

        .detail-icon {
            font-size: 1.5em;
            margin-right: 15px;
            min-width: 30px;
            text-align: center;
        }

        .detail-content {
            flex: 1;
        }

        .detail-label {
            font-weight: 600;
            color: #1a1a1a;
            font-size: 0.95em;
            text-transform: uppercase;
            letter-spacing: 0.5px;
            margin-bottom: 4px;
        }

        .detail-text {
            color: #555;
            font-size: 1em;
        }

        .description {
            background: #f9f7f4;
            padding: 20px;
            border-radius: 8px;
            margin-bottom: 30px;
            font-style: italic;
            color: #555;
            text-align: center;
            line-height: 1.8;
        }

        .dress-code {
            text-align: center;
            margin-bottom: 30px;
            padding: 15px;
            background: rgba(196, 167, 71, 0.08);
            border-radius: 8px;
        }

        .dress-code-label {
            font-weight: 600;
            color: #1a1a1a;
            font-size: 0.9em;
            text-transform: uppercase;
            letter-spacing: 0.5px;
            margin-bottom: 8px;
        }

        .dress-code-text {
            color: #555;
            font-size: 1em;
        }

        .button-group {
            display: flex;
            gap: 12px;
            margin-bottom: 40px;
            flex-wrap: wrap;
        }

        .btn {
            flex: 1;
            min-width: 150px;
            padding: 14px 28px;
            border: none;
            border-radius: 8px;
            font-size: 1em;
            font-weight: 600;
            cursor: pointer;
            transition: all 0.3s ease;
            text-transform: uppercase;
            letter-spacing: 0.5px;
        }

        .btn-primary {
            background: linear-gradient(135deg, #c4a747 0%, #b8941e 100%);
            color: white;
            box-shadow: 0 4px 15px rgba(196, 167, 71, 0.3);
        }

        .btn-primary:hover {
            transform: translateY(-2px);
            box-shadow: 0 6px 20px rgba(196, 167, 71, 0.4);
        }

        .btn-secondary {
            background: #1a1a1a;
            color: white;
            box-shadow: 0 4px 15px rgba(26, 26, 26, 0.2);
        }

        .btn-secondary:hover {
            transform: translateY(-2px);
            box-shadow: 0 6px 20px rgba(26, 26, 26, 0.3);
        }

        .guest-list-section {
            margin-top: 50px;
            padding-top: 40px;
            border-top: 2px solid rgba(196, 167, 71, 0.3);
        }

        .guest-list-section h2 {
            font-family: 'Georgia', serif;
            font-size: 1.8em;
            color: #1a1a1a;
            margin-bottom: 25px;
            text-align: center;
        }

        .form-group {
            margin-bottom: 20px;
        }

        label {
            display: block;
            font-weight: 600;
            color: #1a1a1a;
            margin-bottom: 8px;
            font-size: 0.95em;
        }

        input[type="text"],
        input[type="email"],
        input[type="tel"],
        select {
            width: 100%;
            padding: 12px;
            border: 2px solid #e0dbd3;
            border-radius: 6px;
            font-size: 1em;
            font-family: inherit;
            transition: border-color 0.3s ease;
        }

        input[type="text"]:focus,
        input[type="email"]:focus,
        input[type="tel"]:focus,
        select:focus {
            outline: none;
            border-color: #c4a747;
            box-shadow: 0 0 0 3px rgba(196, 167, 71, 0.1);
        }

        .checkbox-group {
            display: flex;
            align-items: center;
            gap: 10px;
            margin: 15px 0;
        }

        input[type="checkbox"] {
            width: 20px;
            height: 20px;
            cursor: pointer;
            accent-color: #c4a747;
        }

        .checkbox-label {
            margin: 0;
            cursor: pointer;
            font-weight: 500;
        }

        .btn-submit {
            width: 100%;
            padding: 14px;
            background: linear-gradient(135deg, #c4a747 0%, #b8941e 100%);
            color: white;
            border: none;
            border-radius: 8px;
            font-size: 1em;
            font-weight: 600;
            cursor: pointer;
            transition: all 0.3s ease;
            text-transform: uppercase;
            letter-spacing: 0.5px;
            margin-top: 20px;
        }

        .btn-submit:hover {
            transform: translateY(-2px);
            box-shadow: 0 6px 20px rgba(196, 167, 71, 0.4);
        }

        .guest-item {
            background: #f9f7f4;
            padding: 15px;
            border-radius: 6px;
            margin-bottom: 12px;
            border-left: 3px solid #c4a747;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .guest-info {
            flex: 1;
        }

        .guest-name {
            font-weight: 600;
            color: #1a1a1a;
            margin-bottom: 4px;
        }

        .guest-details {
            font-size: 0.9em;
            color: #888;
        }

        .plus-one-badge {
            background: #c4a747;
            color: white;
            padding: 4px 10px;
            border-radius: 20px;
            font-size: 0.85em;
            font-weight: 600;
            margin-left: 10px;
        }

        .success-message {
            background: #e8f5e9;
            color: #2e7d32;
            padding: 15px;
            border-radius: 6px;
            margin-bottom: 20px;
            border-left: 4px solid #4caf50;
            display: none;
        }

        .success-message.show {
            display: block;
            animation: slideIn 0.4s ease-out;
        }

        @media (max-width: 600px) {
            .container {
                padding: 30px 20px;
            }

            h1 {
                font-size: 2em;
            }

            .button-group {
                flex-direction: column;
            }

            .btn {
                min-width: 100%;
            }

            .guest-item {
                flex-direction: column;
                align-items: flex-start;
            }

            .plus-one-badge {
                margin-left: 0;
                margin-top: 10px;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <div class="header">
            <span class="emoji">🎉</span>
            <h1>Susan's Birthday Party</h1>
            <p class="subtitle">You're invited to celebrate!</p>
        </div>

        <div class="details">
            <div class="detail-item">
                <div class="detail-icon">📅</div>
                <div class="detail-content">
                    <div class="detail-label">Date</div>
                    <div class="detail-text">August 19, 2026</div>
                </div>
            </div>

            <div class="detail-item">
                <div class="detail-icon">⏰</div>
                <div class="detail-content">
                    <div class="detail-label">Time</div>
                    <div class="detail-text">6:00 PM – Late Evening</div>
                </div>
            </div>

            <div class="detail-item">
                <div class="detail-icon">📍</div>
                <div class="detail-content">
                    <div class="detail-label">Location</div>
                    <div class="detail-text">Rue du Pont Simon 168<br>7181 Arquennes, Hainaut, Belgium</div>
                </div>
            </div>

            <div class="detail-item">
                <div class="detail-icon">☎️</div>
                <div class="detail-content">
                    <div class="detail-label">Contact</div>
                    <div class="detail-text"><a href="tel:+32493362119" style="color: #c4a747; text-decoration: none;">+32 493 36 21 19</a></div>
                </div>
            </div>
        </div>

        <div class="description">
            We kindly invite you to join us for an evening of celebration, good food, and even better company. Come celebrate Susan's special day in style!
        </div>

        <div class="dress-code">
            <div class="dress-code-label">Dress Code</div>
            <div class="dress-code-text">Smart Casual</div>
        </div>

        <div class="button-group">
            <button class="btn btn-primary" onclick="scrollToRSVP()">RSVP</button>
            <button class="btn btn-secondary" onclick="shareEvent()">Share</button>
        </div>

        <div class="guest-list-section" id="rsvp-section">
            <h2>Guest List</h2>

            <div class="success-message" id="success-message">
                ✓ Thanks for RSVPing! You've been added to the guest list.
            </div>

            <form id="rsvp-form">
                <div class="form-group">
                    <label for="guest-name">Your Name *</label>
                    <input type="text" id="guest-name" name="guest-name" required>
                </div>

                <div class="form-group">
                    <label for="guest-email">Email Address *</label>
                    <input type="email" id="guest-email" name="guest-email" required>
                </div>

                <div class="form-group">
                    <label for="guest-phone">Phone Number</label>
                    <input type="tel" id="guest-phone" name="guest-phone">
                </div>

                <div class="form-group">
                    <label for="dietary">Dietary Restrictions</label>
                    <select id="dietary" name="dietary">
                        <option value="">None</option>
                        <option value="vegetarian">Vegetarian</option>
                        <option value="vegan">Vegan</option>
                        <option value="gluten-free">Gluten-Free</option>
                        <option value="other">Other (please mention in notes)</option>
                    </select>
                </div>

                <div class="form-group">
                    <div class="checkbox-group">
                        <input type="checkbox" id="plus-one-checkbox" name="plus-one">
                        <label for="plus-one-checkbox" class="checkbox-label">I'm bringing a plus one</label>
                    </div>
                </div>

                <div id="plus-one-info" style="display: none;">
                    <div class="form-group">
                        <label for="plus-one-name">Plus One's Name</label>
                        <input type="text" id="plus-one-name" name="plus-one-name">
                    </div>
                </div>

                <button type="submit" class="btn-submit">Confirm RSVP</button>
            </form>

            <div id="guest-list" style="margin-top: 40px;">
                <h3 style="font-family: 'Georgia', serif; color: #1a1a1a; margin-bottom: 20px; font-size: 1.3em;">Guests Attending:</h3>
            </div>
        </div>
    </div>

    <script>
        // Pre-populated guest list with Belgian names
        const belgianGuests = [
            { name: "Amelie Lefevre", dietary: "None", plusOne: false },
            { name: "Martin Moreau", dietary: "Vegetarian", plusOne: false },
            { name: "Sophie Dupont", dietary: "None", plusOne: true, plusOneName: "Antoine Rousseau" },
            { name: "Jean-Pierre Dubois", dietary: "None", plusOne: false },
            { name: "Claire Renard", dietary: "Gluten-Free", plusOne: false },
            { name: "Nicolas Lacroix", dietary: "None", plusOne: false },
            { name: "Isabelle Fontaine", dietary: "Vegan", plusOne: true, plusOneName: "Thomas Mercier" },
            { name: "Laurent Desmet", dietary: "None", plusOne: false },
            { name: "Margot Blanchard", dietary: "None", plusOne: false },
            { name: "Pierre Godard", dietary: "None", plusOne: false }
        ];

        let guests = [...belgianGuests];

        function renderGuestList() {
            const guestListDiv = document.getElementById('guest-list');
            const guestItemsHtml = guests.map(guest => {
                let html = `<div class="guest-item">
                    <div class="guest-info">
                        <div class="guest-name">${guest.name}</div>
                        <div class="guest-details">${guest.dietary !== 'None' ? `Dietary: ${guest.dietary}` : 'No dietary restrictions'}</div>
                    </div>`;
                if (guest.plusOne) {
                    html += `<div class="plus-one-badge">+1</div>`;
                }
                html += `</div>`;
                return html;
            }).join('');

            guestListDiv.innerHTML = `<h3 style="font-family: 'Georgia', serif; color: #1a1a1a; margin-bottom: 20px; font-size: 1.3em;">Guests Attending:</h3>${guestItemsHtml}`;
        }

        function scrollToRSVP() {
            document.getElementById('rsvp-section').scrollIntoView({ behavior: 'smooth' });
        }

        function shareEvent() {
            const eventText = "You're invited to Susan's Birthday Party on August 19, 2026 at Rue du Pont Simon 168, Arquennes, Belgium!";
            if (navigator.share) {
                navigator.share({
                    title: "Susan's Birthday Party",
                    text: eventText
                });
            } else {
                alert("Event: Susan's Birthday Party\nDate: August 19, 2026\nLocation: Rue du Pont Simon 168, 7181 Arquennes, Hainaut, Belgium\n\nCopy and share this info!");
            }
        }

        document.getElementById('plus-one-checkbox').addEventListener('change', function() {
            document.getElementById('plus-one-info').style.display = this.checked ? 'block' : 'none';
        });

        document.getElementById('rsvp-form').addEventListener('submit', function(e) {
            e.preventDefault();

            const name = document.getElementById('guest-name').value;
            const email = document.getElementById('guest-email').value;
            const dietary = document.getElementById('dietary').value || 'None';
            const hasPlusOne = document.getElementById('plus-one-checkbox').checked;
            const plusOneName = hasPlusOne ? document.getElementById('plus-one-name').value : null;

            const newGuest = {
                name: name,
                dietary: dietary,
                plusOne: hasPlusOne,
                plusOneName: plusOneName || null
            };

            guests.push(newGuest);
            renderGuestList();

            // Show success message
            const successMessage = document.getElementById('success-message');
            successMessage.classList.add('show');
            setTimeout(() => {
                successMessage.classList.remove('show');
            }, 4000);

            // Reset form
            this.reset();
            document.getElementById('plus-one-info').style.display = 'none';
        });

        // Initial render
        renderGuestList();
    </script>
