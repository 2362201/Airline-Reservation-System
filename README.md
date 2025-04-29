# Airline-Reservation-System
# MAIN PAGE
<!DOCTYPE html>
<html lang="en">

<head>
  <meta charset="UTF-8" />
  <title>Airline Reservation System</title>
  <link rel="stylesheet" href="flight.css" />
  <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.5/dist/css/bootstrap.min.css" rel="stylesheet"
    integrity="sha384-SgOJa3DmI69IUzQ2PVdRZhwQ+dy64/BUtbMJw1MZ8t5HZApcHrRKUc4W0kG879m7" crossorigin="anonymous">
  <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.5/dist/js/bootstrap.bundle.min.js"
    integrity="sha384-k6d4wzSIapyDyv1kpU366/PK5hCdSbCRGRCMv+eplOQJWyd1fbcAu9OCUj5zNLiq"
    crossorigin="anonymous"></script>
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">

  <script src="Airline.js" defer></script>
  <script src="client.js"></script>
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
  <link rel="stylesheet" href="style1.css">
  <script src="script2.js"></script>
  <link rel="stylesheet" href="Airline.css">
  <!-- <link rel="stylesheet" href="booking-success.css"> -->
  <!-- <script src="booking-success.js"></script> -->
  <!-- <link rel="stylesheet" href="booking_confirmation.css"> -->
  <!-- <script src="booking_confirmation.js"></script> -->
   <!-- <link rel="stylesheet" href="booking.css"> -->
  <script src="backend.js"></script>
  <!-- Leaflet CSS for live map -->
  <link rel="map" href="https://unpkg.com/leaflet@1.9.4/dist/leaflet.css" />
</head>

<body>
  <video autoplay muted loop class="video-background">
    <source src="assets/Video.mp4" type="video/mp4">
    Your browser does not support the video tag.
  </video>
  <div class="background"></div>
  <h2>Your Experience Starts Here!</h2>
  <nav class="navbar">
    <div class="navbar-container">
      <div class="navbar-logo">
        <a href="index.html"><i class="fas fa-plane-departure"></i> FlyAway</a>
      </div>
      <!-- Hamburger toggle -->
      <div class="hamburger" id="hamburger">
        <i class="fas fa-bars"></i>
      </div>

      <!-- Links -->
      <div class="navbar-links" id="navbarLinks">
        <a href="flights.html"><i class="fas fa-plane"></i> Flights</a>
        <a href="hotels.html"><i class="fas fa-hotel"></i> Hotels</a>
        <a href="trains.html"><i class="fas fa-train"></i> Trains</a>
        <a href="cabs.html"><i class="fas fa-taxi"></i> Cabs</a>
        <a href="bus.html"><i class="fas fa-bus"></i> Bus</a>
        <a href="holidays.html"><i class="fas fa-umbrella-beach"></i> Holidays</a>
        <a href="forex.html"><i class="fas fa-dollar-sign"></i> Forex</a>
        <a href="login.html"><i class="fas fa-sign-in-alt"></i> Login</a>
      </div>

      <!-- Leaflet JS for map functionality -->
      <script src="https://unpkg.com/leaflet@1.9.4/dist/leaflet.js"></script>

  </nav>
  <div class="collapse" id="navbarToggleExternalContent">
    <div class="bg-body-tertiary shadow-3 p-4">
      <button data-mdb-button-init data-mdb-ripple-init class="btn btn-link btn-block border-bottom m-0">Link 1</button>
      <button data-mdb-button-init data-mdb-ripple-init class="btn btn-link btn-block border-bottom m-0">Link 2</button>
      <button data-mdb-button-init data-mdb-ripple-init class="btn btn-link btn-block m-0">Link
        3</button>
    </div>
  </div>



  <h2>Airline Reservation System</h2>

  <div id="flight-section" class="form-container">
    <form id="flightForm">
      <fieldset>
        <h1>Trip Details</h1>

        <div class="trip-type">
          <label><input type="radio" name="trip" value="one-way" checked /> One-way</label>
          <label><input type="radio" name="trip" value="round-trip" /> Round-trip</label>
          <label><input type="radio" name="trip" value="multi-city" /> Multi-city</label>
        </div>
        <div class="form-content with-arrow">
          <!-- Arrow button here -->

          <div class="form-content with-arrow">
            <div class="form-group">
              <label for="source">Your Journey:</label>
              <input type="text" id="source" name="source" placeholder="Enter your source...." />
              </select>
              <span class="margin"><svg width="25" height="40" fill="none" xmlns="http://www.w3.org/2000/svg"
                  style="transform: rotate(90deg);">
                  <path
                    d="M14.11 6.739a.842.842 0 0 1-.842-.842V4.844a.21.21 0 0 0-.21-.211H4.543a1.264 1.264 0 1 1 0-2.527h8.515a.21.21 0 0 0 .21-.21V.841A.843.843 0 0 1 14.544.12l4.212 2.528a.842.842 0 0 1 0 1.444L14.544 6.62a.843.843 0 0 1-.433.12ZM.409 10.26l4.212-2.527a.842.842 0 0 1 1.276.723v1.053c0 .116.095.21.21.21h8.516a1.264 1.264 0 1 1 0 2.528H6.108a.21.21 0 0 0-.21.21v1.053a.842.842 0 0 1-1.277.722L.409 11.705a.842.842 0 0 1 0-1.445Z"
                    fill="#2276E3" />
                </svg></span>
            </div>

            <div class="form-group">
              <input type="text" id="source" name="source" placeholder="Enter your destination...." />
              </select>
            </div>
          </div>
        </div>
        <div class="form-group">
          <label for="travellers">Travellers:</label>
          <input type="number" value="1" min="1" id="travellers" name="travellers" required />
        </div>

        <div class="form-group">
          <label for="class">Class:</label>
          <select id="class" name="class" required>
            <option value="General">General</option>
            <option value="Economy">Economy</option>
            <option value="Premium Economy">Premium Economy</option>
            <option value="Business">Business Class</option>
          </select>
        </div>

        <div class="form-group">
          <label for="offers">Offers:</label>
          <input type="text" id="offers" name="offers" placeholder="E.g., NewUser, SummerSale" />
        </div>
        <div class="form-group">
          <label for="departureDate">Departure Date:</label>
          <input type="date" id="departureDate" name="departureDate" required />
        </div>

        <button id="bookFlightBtn" class="btn btn-primary">Book flight</button>
        <button id="searchFlightBtn" class="btn btn-primary">Search flight</button>

        <div id="results-section" style="display: none;">
          <h3 id="results-title"></h3>
          <div id="results-container"></div>
          <button id="backBtn">← Back</button>
        </div>
      </fieldset>
    </form>


    <div class="trip-type">
      <label><input type="checkbox" name="category1" /> Student</label>
      <label><input type="checkbox" name="category2" /> Senior citizen</label>
      <label><input type="checkbox" name="category3" /> Armed forces</label>
      <label><input type="checkbox" name="category4" /> Doctors & Nurses</label>
    </div>
  </div>

  <section id="results-section">
    <h2 id="results-title"></h2>
    <div id="results-container"></div>
    <br>
    <button id="backBtn">Back</button>
  </section>
  <div class="form-group" id="returnDateGroup" style="display: none;">
    <label for="returnDate">Return Date:</label>
    <input type="date" id="returnDate" name="returnDate" />
  </div>
  <footer class="footer">
    <h3>Popular Flight Routes</h3>
    <div class="routes-grid">
      <div class="route-box">
        <strong>Delhi</strong>
        <p>
          From:
          <a href="#">Mumbai</a>,
          <a href="#">Pune</a>,
          <a href="#">Bangalore</a>,
          <a href="#">Goa</a>
        </p>
      </div>
      <div class="route-box">
        <strong>Mumbai</strong>
        <p>
          From:
          <a href="#">Delhi</a>,
          <a href="#">Ahmedabad</a>,
          <a href="#">Bangalore</a>,
          <a href="#">Chennai</a>
        </p>
      </div>
      <div class="route-box">
        <strong>Bangalore</strong>
        <p>
          From:
          <a href="#">Mumbai</a>,
          <a href="#">Kolkata</a>,
          <a href="#">Delhi</a>,
          <a href="#">Pune</a>
        </p>
      </div>
      <div class="route-box">
        <strong>Goa</strong>
        <p>
          From:
          <a href="#">Mumbai</a>,
          <a href="#">Pune</a>,
          <a href="#">Delhi</a>,
          <a href="#">Indore</a>
        </p>
      </div>
      <div class="route-box">
        <strong>Jaipur</strong>
        <p>
          From:
          <a href="#">Mumbai</a>,
          <a href="#">Ahmedabad</a>,
          <a href="#">Pune</a>,
          <a href="#">Bangalore</a>
        </p>
      </div>
      <div class="route-box">
        <strong>Kolkata</strong>
        <p>
          From:
          <a href="#">Mumbai</a>,
          <a href="#">Hyderabad</a>,
          <a href="#">Delhi</a>,
          <a href="#">Bangalore</a>
        </p>
      </div>
      <div class="route-box">
        <strong>Pune</strong>
        <p>
          From:
          <a href="#">Delhi</a>,
          <a href="#">Kolkata</a>,
          <a href="#">Nagpur</a>,
          <a href="#">Bangalore</a>
        </p>
      </div>
      <div class="route-box">
        <strong>Hyderabad</strong>
        <p>
          From:
          <a href="#">Mumbai</a>,
          <a href="#">Delhi</a>,
          <a href="#">Kolkata</a>,
          <a href="#">Bangalore</a>
        </p>
      </div>
      <div class="route-box">
        <strong>Chennai</strong>
        <p>
          From:
          <a href="#">Mumbai</a>,
          <a href="#">Hyderabad</a>,
          <a href="#">Delhi</a>,
          <a href="#">Coimbatore</a>
        </p>
      </div>
      <div class="route-box">
        <strong>Ahmedabad</strong>
        <p>
          From:
          <a href="#">Delhi</a>,
          <a href="#">Mumbai</a>,
          <a href="#">Bangalore</a>,
          <a href="#">Pune</a>
        </p>
      </div>
      <div class="route-box">
        <strong>Patna</strong>
        <p>
          From:
          <a href="#">Delhi</a>,
          <a href="#">Bangalore</a>,
          <a href="#">Mumbai</a>,
          <a href="#">Kolkata</a>
        </p>
      </div>
      <div class="route-box">
        <strong>Lucknow</strong>
        <p>
          From:
          <a href="#">Delhi</a>,
          <a href="#">Mumbai</a>,
          <a href="#">Bangalore</a>,
          <a href="#">Pune</a>
        </p>
      </div>
    </div>
  </footer>
  <section class="faq">
    <h2>Frequently Asked Questions</h2>

    <div class="faq-item">
      <h3>What documents are needed for airline travel?</h3>
      <p>You’ll need a valid government-issued ID or passport for booking and check-in. International flights may also
        require additional documents such as visas or vaccination certificates.</p>
    </div>

    <div class="faq-item">
      <h3>Can I cancel or reschedule my flight?</h3>
      <p>Yes, most airlines allow cancellations or changes, but fees may apply depending on the fare rules. Always
        review your ticket terms and conditions before booking.</p>
    </div>

    <div class="faq-item">
      <h3>What is the baggage allowance?</h3>
      <p>Each airline has specific baggage policies, which typically include a carry-on allowance and a checked baggage
        limit. Additional charges may apply for oversized or extra baggage.</p>
    </div>

    <div class="faq-item">
      <h3>How do I check in for my flight?</h3>
      <p>Most airlines offer online check-in 24-48 hours before departure. Alternatively, you can check in at the
        airport counter or self-service kiosks on the day of departure.</p>
    </div>

    <div class="faq-item">
      <h3>Can I request special assistance?</h3>
      <p>Yes, airlines provide special services such as wheelchair assistance, priority boarding, and customized meals
        for dietary needs. Contact the airline at least 24 hours before your flight.</p>
    </div>

    <div class="faq-item">
      <h3>How can I select or upgrade my seat?</h3>
      <p>You can select your seat during booking or through the airline’s online check-in portal. Upgrades to premium or
        business class may be available for an additional fee.</p>
    </div>

    <div class="faq-item">
      <h3>Is travel insurance necessary?</h3>
      <p>While not mandatory, travel insurance is highly recommended. It covers unexpected incidents such as flight
        cancellations, lost baggage, or medical emergencies.</p>
    </div>
  </section>
  </div>

  <script>
    /* Include your JS here  */
  </script>
  <footer>
    <div class="footer-box">
      <footer>
        <div class="footer-container">
          <div class="footer-column">
            <h3>OUR PRODUCTS</h3>
            <ul>
              <li><a href="#">Domestic Hotels</a></li>
              <li><a href="#">International Hotels</a></li>
              <li><a href="#">Domestic Flights</a></li>
              <li><a href="#">International Flights</a></li>
              <li><a href="#">Multi-City Flights</a></li>
              <li><a href="#">Couple Friendly Hotels</a></li>
              <li><a href="#">Nearby Getaways</a></li>
            </ul>
          </div>
          <div class="footer-column">
            <h3>ABOUT US</h3>
            <ul>
              <li><a href="#">About Us</a></li>
              <li><a href="#">Investor Relations</a></li>
              <li><a href="#">Terms of Services</a></li>
              <li><a href="#">Privacy</a></li>
              <li><a href="#">Careers</a></li>
              <li><a href="#">Advertise with Us</a></li>
            </ul>
          </div>
          <div class="footer-column">
            <h3>TRAVEL ESSENTIALS</h3>
            <ul>
              <li><a href="#">PNR Status</a></li>
              <li><a href="#">Offers</a></li>
              <li><a href="#">Airline Routes</a></li>
              <li><a href="#">Train Running Status</a></li>
            </ul>
          </div>
          <div class="footer-column">
            <h3>MORE LINKS</h3>
            <ul>
              <li><a href="#">Cheap Flights</a></li>
              <li><a href="#">Hotels Near Me</a></li>
              <li><a href="#">My Bookings</a></li>
              <li><a href="#">Cancellation</a></li>
            </ul>
          </div>
        </div>
      </footer>
    </div>
    <hr>

    <footer>
      <div class="last">
        <h4>Follow Us</h4>
        <div class="social-icons">
          <a target="_blank" href="http://www.facebook.com/goibibo" title="Facebook" aria-label="Facebook">
            <span class="footer-sprite facebookIcon"></span>
          </a>
          <a target="_blank" href="http://twitter.com/goibibo" title="Twitter" aria-label="Twitter">
            <span class="footer-sprite twitterIcon"></span>
          </a>
          <a target="_blank" href="https://plus.google.com/+goibibo/" title="Google Plus" aria-label="Google Plus">
            <span class="footer-sprite gplusIcon"></span>
          </a>
          <a target="_blank" href="http://www.youtube.com/user/goibibo" title="YouTube" aria-label="YouTube">
            <span class="footer-sprite youtubeIcon"></span>
          </a>
        </div>

        <h4>Book Tickets Faster. Download our Mobile Apps</h4>
        <div class="store-icons">
          <a href="https://play.google.com/store/apps/details?id=com.goibibo" target="_blank" rel="noreferrer">
            <img src="https://upload.wikimedia.org/wikipedia/commons/7/78/Google_Play_Store_badge_EN.svg" width="120"
              alt="Google Play">
          </a>
          <a href="https://apps.apple.com/in/app/goibibo-flight-bus-hotel-booking/id631927169" target="_blank"
            rel="noreferrer">
            <img src="https://developer.apple.com/assets/elements/badges/download-on-the-app-store.svg" width="120"
              alt="App Store">
          </a>
        </div>

        <div class="payment-icons">
          <span class="footer-sprite verifySign">&nbsp;</span>
          <span class="footer-sprite amricanIcon">&nbsp;</span>
          <span class="footer-sprite masterCardIcon">&nbsp;</span>
          <span class="footer-sprite visaIcon">&nbsp;</span>
          <span class="footer-sprite ruPayIcon">&nbsp;</span>
          <span class="footer-sprite iataIcon">&nbsp;</span>
        </div>
      </div>
      <!-- Live Flight Status Ticker -->
      <section class="ticker-wrapper">
        <div id="ticker" class="ticker">
          <ul id="flightStatusList"></ul>
        </div>
      </section>
      <script src="https://checkout.razorpay.com/v1/checkout.js"></script>

      <script src="https://checkout.razorpay.com/v1/checkout.js"></script>
      <script>
        // Initialize Map
        const map = L.map('map').setView([20.5937, 78.9629], 3);

        L.tileLayer('https://{s}.tile.openstreetmap.org/{z}/{x}/{y}.png', {
          maxZoom: 19,
          attribution: '© OpenStreetMap'
        }).addTo(map);

        const planesLayer = L.layerGroup().addTo(map);

        async function fetchPlanes() {
          try {
            const response = await fetch('https://opensky-network.org/api/states/all');
            const data = await response.json();

            planesLayer.clearLayers();

            if (data.states) {
              data.states.forEach(plane => {
                const latitude = plane[6];
                const longitude = plane[5];
                const callsign = plane[1];

                if (latitude && longitude) {
                  const marker = L.marker([latitude, longitude], {
                    icon: L.icon({
                      iconUrl: 'https://img.icons8.com/ios-filled/50/000000/airplane-take-off.png',
                      iconSize: [25, 25],
                      iconAnchor: [12, 12]
                    })
                  }).bindPopup(`<b>Flight:</b> ${callsign || "Unknown"}`);
                  planesLayer.addLayer(marker);
                }
              });
            }
          } catch (error) {
            console.error('Error fetching plane data:', error);
          }
        }

        // Fetch initially and then update every 10 seconds
        fetchPlanes();
        setInterval(fetchPlanes, 10000);
        document.addEventListener('DOMContentLoaded', function () {

          // --- Booking Form Submit (save source and destination)
          const bookingForm = document.getElementById('bookingForm');
          if (bookingForm) {
            bookingForm.addEventListener('submit', function (event) {
              event.preventDefault();
              const source = document.getElementById('source').value.trim();
              const destination = document.getElementById('destination').value.trim();
              if (!source || !destination) {
                alert('Please fill in Source and Destination!');
                return;
              }
              localStorage.setItem('source', source);
              localStorage.setItem('destination', destination);
              window.location.href = 'booking_confirmation.html';
            });
          }

          // --- Search Flights Button
          const searchBtn = document.getElementById('searchBtn1');
          if (searchBtn) {
            searchBtn.addEventListener('click', function (event) {
              event.preventDefault();
              const source = document.getElementById('source').value.trim();
              const destination = document.getElementById('destination').value.trim();
              const travellers = document.getElementById('travellers').value.trim();
              const departureDate = document.getElementById('departureDate').value.trim();

              if (!source || !destination || !travellers || !departureDate) {
                alert('Please fill in all fields!');
                return;
              }

              const resultsSection = document.getElementById('results-section');
              const resultsTitle = document.getElementById('results-title');
              const resultsContainer = document.getElementById('results-container');

              if (resultsTitle && resultsContainer && resultsSection) {
                resultsTitle.textContent = `Searching flights from ${source} to ${destination}`;
                resultsContainer.innerHTML = `<p>Searching for flights from ${source} to ${destination}... Please wait.</p>`;
                resultsSection.style.display = 'block';
              }
            });
          }

          // --- Back Button to hide search results
          const backBtn = document.getElementById('backBtn');
          if (backBtn) {
            backBtn.addEventListener('click', function () {
              const resultsSection = document.getElementById('results-section');
              if (resultsSection) {
                resultsSection.style.display = 'none';
              }
            });
          }

          // --- Book Flight Button with Razorpay Payment
          const bookBtn = document.getElementById('bookBtn1');
          if (bookBtn) {
            bookBtn.addEventListener('click', async function (event) {
              event.preventDefault();

              const source = document.getElementById('source').value.trim();
              const destination = document.getElementById('destination').value.trim();
              const travelDate = document.getElementById('departureDate').value.trim();

              if (!source || !destination || !travelDate) {
                alert("Please fill Source, Destination, and Travel Date!");
                return;
              }

              // Save booking data to localStorage
              localStorage.setItem('source', source);
              localStorage.setItem('destination', destination);
              localStorage.setItem('travelDate', travelDate);

              try {
                const response = await fetch('http://localhost:5000/create-order', {
                  method: 'POST',
                  headers: { 'Content-Type': 'application/json' },
                  body: JSON.stringify({ amount: 500 })
                });

                const order = await response.json();

                const options = {
                  key: "YOUR_RAZORPAY_KEY_ID", // replace with your Razorpay key
                  amount: order.amount,
                  currency: "INR",
                  name: "Airline Reservation",
                  description: `Flight from ${source} to ${destination}`,
                  order_id: order.id,
                  handler: function (response) {
                    alert("Payment Successful! Payment ID: " + response.razorpay_payment_id);
                    window.location.href = "booking-confirmation.html";
                  },
                  prefill: {
                    name: "John Doe",
                    email: "john@example.com",
                    contact: "9999999999"
                  },
                  theme: {
                    color: "#3399cc"
                  }
                };

                const rzp = new Razorpay(options);
                rzp.open();

              } catch (error) {
                console.error("Error creating order:", error);
                alert("Something went wrong during booking. Please try again!");
              }
            });
          }

          // --- Separate Search Button (with inputs: sourceInput, destinationInput, etc.)
          const separateSearchBtn = document.getElementById('searchButton');
          if (separateSearchBtn) {
            separateSearchBtn.addEventListener('click', function () {
              const source = document.getElementById('sourceInput').value.trim();
              const destination = document.getElementById('destinationInput').value.trim();
              const departureDate = document.getElementById('departureDateInput').value.trim();
              const travelClass = document.getElementById('travelClass').value.trim();

              if (!source || !destination || !departureDate || !travelClass) {
                alert("Please fill in all fields!");
                return;
              }

              const searchURL = `searchResults.html?source=${encodeURIComponent(source)}&destination=${encodeURIComponent(destination)}&departureDate=${encodeURIComponent(departureDate)}&class=${encodeURIComponent(travelClass)}`;
              window.open(searchURL, "_blank");
            });
          }

          // --- Flight Search Form Submit (separate)
          const flightSearchForm = document.getElementById('flightSearchForm');
          if (flightSearchForm) {
            flightSearchForm.addEventListener('submit', function (event) {
              event.preventDefault();

              const from = document.querySelector('[name="from"]').value.trim();
              const to = document.querySelector('[name="to"]').value.trim();
              const departure = document.querySelector('[name="departure"]').value.trim();

              if (!from || !to || !departure) {
                alert('Please fill all fields!');
                return;
              }

              const searchUrl = `searchResults.html?from=${encodeURIComponent(from)}&to=${encodeURIComponent(to)}&departure=${encodeURIComponent(departure)}`;
              window.location.href = searchUrl;
            });
          }

        });
      </script>

</body>

<script src="js/Airline.js"></script>

</html>

* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

#navbar {
  position: sticky;
  top: 0;
  overflow: hidden;
  background-color: #333;
}

img {
  display: none;
  /* Hide the img tag if you're using it as background */
}

/* Quick basic styles */
#navbarLinks.active,
#sidebar.active,
#returnDateGroup,
#results-section {
  display: block;
}

#returnDateGroup,
#results-section {
  display: none;
}

#sidebar {
  position: fixed;
  top: 0;
  left: -250px;
  width: 250px;
  background: #eee;
  height: 100%;
  transition: left 0.3s;
}

#sidebar.active {
  left: 0;
}


h1 {
  position: relative;
  z-index: 1;
  /* Make sure the text appears above the background */
}


h1,
h2 {
  text-align: center;
  margin: 20px 10px;
  text-shadow: 2px 2px 2px #ffffff;

}

.top-navbar {
  background-color: #b9bdd8;
  width: 100%;
  padding: 5px;
  display: flex;
  justify-content: center;
  flex-wrap: wrap;
  position: sticky;
  top: 0;
  z-index: 10;
}

.top-navbar a {
  font-weight: bold;
  text-decoration: none;
  transition: transform 0.2s ease;
}

.top-navbar a:hover {
  color: #28a745;
  transform: scale(1.1);
}

.form-container {
  background-color: rgba(0, 0, 0, 0.7);
  border-radius: 10px;
  padding: 30px 20px;
  margin-top: 20px;
  width: 90%;
  max-width: 500px;
  box-shadow: 0 0 15px rgba(0, 0, 0, 0.4);
  display: flex;
  flex-direction: column;
  gap: 15px;
}

fieldset {
  border: none;
}

legend {
  font-size: 20px;
  font-weight: bold;
  margin-bottom: 10px;
}

.form-group {
  display: flex;
  flex-direction: column;
  gap: 5px;
}

label {
  font-weight: bold;
  font-size: 14px;
}

input,
select {
  padding: 10px;
  font-size: 14px;
  border: none;
  border-radius: 5px;
  outline: none;
  cursor: pointer;
}

input[type="submit"],
button {
  background-color: #2E7D32;
  display: inline-flex;
  align-items: center;
  justify-content: center;
  color: white;
  font-weight: 600;
  line-height: normal;
  font-size: 11px;
  padding: 3px 9px;
  border: 0px;
  margin-left: 15px;
  margin-top: 12px;
  line-height: normal;
  /* font-size: 16px; */
  width: 16%;
  border-radius: 30px;
  cursor: pointer;
  transition: background-color 0.3s ease;
}

button:hover,
input[type="submit"]:hover {
  background-color: #3c7202;
  align-items: left;
}

.trip-type {
  display: flex;
  flex-wrap: wrap;
  gap: 10px;
  margin-top: 10px;
  margin-bottom: 30px;
}

.trip-type label {
  display: flex;
  align-items: center;
  gap: 5px;
  font-weight: bold;
  color: #ddd;
}

.card {
  background-color: #fff;
  color: #000;
  padding: 15px;
  border-radius: 8px;
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.3);
  margin-bottom: 15px;
  transition: transform 0.2s ease;
}

.card:hover {
  transform: scale(1.03);
}

#results-section {
  width: 90%;
  max-width: 600px;
  background-color: rgba(255, 255, 255, 0.9);
  padding: 30px;
  border-radius: 10px;
  margin-top: 20px;
  color: #000;
}

#results-section h3 {
  text-align: center;
  color: #004080;
  margin-bottom: 20px;
}

.footer {
  width: 100%;
  background-color: rgb(255 179 0 / 48%);
  color: #222;
  padding: 20px;
  text-align: left;
  margin-top: 20px;
}

.footer h3 {
  font-size: 18px;
  margin-bottom: 10px;
}

.footer ul li {
  margin-bottom: 5px;
  font-size: 14px;
}

.swap-button {
  text-align: center;

  width: 40px;
  height: 40px;
  background-color: white;
  border-radius: 12px;
  display: flex;
  align-items: center;
  justify-content: center;
  /* display: inline; */
  margin-left: 30px;
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
  cursor: pointer;
  transition: box-shadow 0.3s ease;
}

.swap-button:hover {
  box-shadow: 0 6px 12px rgba(0, 0, 0, 0.15);
}

.swap-button i {
  color: #1a73e8;
  /* Google-like blue */
  font-size: 16px;
}

.margin {
  /* margin-left: 190px; */
  background-color: white;
  /* z-index: 8; */
  margin: auto;
  width: 50px;
  margin-top: -15px;
}

/* Responsive */
@media (max-width: 768px) {
  .top-navbar {
    flex-direction: column;
    gap: 10px;
    align-items: center;
  }

  .form-container {
    width: 95%;
  }

  #results-section {
    width: 95%;
  }

  .trip-type {
    flex-direction: column;
    align-items: flex-start;

  }
}

@media (max-width: 480px) {
  h1 {
    font-size: 22px;

  }

  h2 {
    font-size: 18px;
  }

  input,
  select,
  button {
    font-size: 14px;
  }

  .top-navbar {
    font-size: 14px;
  }
}

.navbar {
  display: flex;
  justify-content: space-between;
  /* Ensures separation between menu and button */
  align-items: center;
  padding: 10px 20px;
  /* background-color: #f8f8f8; */
}

.menu {
  display: flex;
  gap: 15px;
  /* Adds spacing between menu items */
}

.menu a {
  text-decoration: none;
  color: black;
  font-weight: bold;
}

.routes-grid {
  display: flex;
  flex-wrap: wrap;
  gap: 20px;
  justify-content: space-around;
  margin-top: 20px;
}

.route-box {
  background-color: #e8e4bca8;
  padding: 15px;
  border-radius: 10px;
  min-width: 220px;
  max-width: 250px;
  flex: 1 1 220px;
  box-shadow: 0 2px 8px rgba(0, 0, 0, 0.15);
  color: #000;
}

.route-box a {
  text-decoration: none;
  font-weight: 500;
}

.route-box a:hover {
  text-decoration: underline;
}

.route-box a:visited {
  color: #e81a70;
}

.faq-container {
  max-width: 800px;
  margin: 20px auto;
  padding: 1rem;
  font-family: Arial, sans-serif;
}

.faq-item {
  border: 1px solid #ddd;
  border-radius: 8px;
  margin-bottom: 10px;
  overflow: hidden;
}

.faq-question {
  padding: 15px;
  background-color: #f95757;
  cursor: pointer;
  font-weight: bold;
  transition: background-color 0.3s;
}

.faq-question .toggle {
  font-size: 1.2rem;
  color: #007bff;
  margin-left: 10px;
}

.faq-question:hover {
  background-color: #8a7a7a;
}

.faq-answer {
  padding: 15px;
  display: none;
  /* Hidden by default */
  background-color: #964949;
  border-top: 1px solid #ddd;
}

/* Hide nav links by default on small screens */
.top-navbar a {
  display: inline-block;
  padding: 0.5rem 1rem;
  text-decoration: none;
  color: #333;
}

/* Hamburger lines */
.burger {
  display: none;
  flex-direction: column;
  cursor: pointer;
}

.burger .line {
  width: 25px;
  height: 3px;
  background-color: #333;
  margin: 4px 0;
}

/* Responsive behavior */
@media (max-width: 768px) {
  .burger {
    display: flex;
  }

  .top-navbar {
    flex-direction: column;
    max-height: 60px;
    /* Initially collapsed */
    overflow: hidden;
  }

  .top-navbar.show {
    max-height: 500px;
    /* Show all items */
  }

  .top-navbar a {
    display: block;
    width: 100%;
    text-align: left;
  }
}

.h-nav {
  height: 72px;
}

.v-class {
  opacity: 0;
}

/* Base nav styles */
.nav-links {
  display: flex;
  gap: 1rem;
  align-items: center;
}

/* General styles */
body {
  margin: 0;
  font-family: Arial, sans-serif;
}

/* Header styling */
.nav-container {
  display: flex;
  justify-content: space-between;
  align-items: center;
  background-color: #4c1570;
  padding: 10px 20px;
  color: #fff;
}

h1 {
  font-size: 24px;
  margin: 0;

}

/* Hamburger styles */
.hamburger {
  display: none;
  flex-direction: column;
  justify-content: space-between;
  width: 25px;
  height: 20px;
  background: none;
  border: none;
  cursor: pointer;
  z-index: 10;
}

.hamburger span {
  display: block;
  width: 100%;
  height: 3px;
  background-color: #fff;
  transition: all 0.3s ease;
}

/* Navigation links */
.nav-links {
  display: flex;
  gap: 20px;
}

.nav-links a {
  text-decoration: none;
  color: #fff;
  font-weight: bold;
  transition: color 0.3s;
}

.nav-links a:hover {
  color: #00bcd4;
}

/* Responsive styles */
@media (max-width: 768px) {
  .hamburger {
    display: flex;
  }

  .nav-links {
    position: absolute;
    top: 50px;
    right: 0;
    background-color: #4c1570;
    flex-direction: column;
    gap: 15px;
    width: 200px;
    padding: 10px;
    display: none;
  }

  .nav-links.open {
    display: flex;
  }
}

.footer {
  /* Light background */
  padding: 20px;
}

.footer-box {
  background-color: #4677a8;
  /* Light background for footer box */
  border: 1px solid #ddd;
  /* Adds a border around the footer box */
  padding: 20px;
  max-width: 1200px;
  /* Optional: Sets the width limit for the box */
  margin: 20px auto;
  /* Centers the footer box */
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
  /* Gives a subtle shadow effect */
}

.footer-container {
  display: flex;
  flex-wrap: wrap;
  /* Makes it responsive */
  justify-content: space-between;
  /* Even spacing between columns */
}

.footer-column {
  width: 22%;
  /* Adjust the column width */
  margin-bottom: 20px;
  /* Adds spacing between rows */
}

.footer-column h3 {
  font-size: 16px;
  margin-bottom: 10px;
}

.footer-column ul {
  list-style: none;
  padding: 0;
}

.footer-column ul li {
  margin-bottom: 8px;
}

.footer-column ul li a {
  text-decoration: none;
  color: #000;
  /* Link color */
  font-size: 14px;
}

.footer-column ul li a:hover {
  text-decoration: underline;
  /* Adds hover effect */
  color: #007bff;
  /* Change color on hover */
}

@media (max-width: 768px) {
  .footer-column {
    width: 48%;
    /* Make it fit two columns on smaller screens */
  }
}

@media (max-width: 480px) {
  .footer-column {
    width: 100%;
    /* Full width for mobile */
  }
}

@media (max-width: 768px) {
  .footer-column {
    width: 48%;
    /* Make it fit two columns on smaller screens */
  }
}

@media (max-width: 480px) {
  .footer-column {
    width: 100%;
    /* Full width for mobile */
  }
}

.last {
  display: flex;
  /* Arranges items in a row */
  justify-content: center;
  /* Centers the items horizontally */
  align-items: center;
  /* Aligns items vertically */
  gap: 4rem;
  /* Adds spacing between the items */
}

.last h4 {
  margin: 0;
  /* Removes default margin for the headings */
}

.logo-container {
  display: flex;
  align-items: center;
  gap: 20px;
  padding: 10px;
}

.logo-container img {
  height: 40px;
  cursor: pointer;
}


footer {
  margin-top: 20px;
  background-color: #865353;
  color: #333;
  padding: 48px 20px;
  font-family: Arial, sans-serif;
}

.last h4 {
  margin-bottom: 10px;
  color: #222;
}

.social-icons,
.store-icons,
.payment-icons,
.logo-container {
  display: flex;
  gap: 15px;
  align-items: center;
  flex-wrap: wrap;
  margin: 10px 0;
}

.footer-sprite {
  display: inline-block;
  width: 32px;
  height: 32px;
  background-color: #ccc;
  /* Placeholder, use icons in your actual CSS */
  border-radius: 50%;
}

.store-icons img,
.logo-container img {
  height: 40px;
  transition: transform 0.3s ease;
}

.footer-sprite,
.logo-container img {
  cursor: pointer;
}

.enlarged {
  transform: scale(1.3);
}

hr {
  border: none;
  border-top: 1px solid #ccc;
  margin: 30px 0;
}

.logo-container {
  justify-content: center;
}

.footer-copyright {
  text-align: center;
  margin-top: 20px;
  font-size: 14px;
  color: #666;
}

/* Main container */
.faq-container {
  max-width: 800px;
  margin: 40px auto;
  padding: 20px;
  background-color: #f9f9f9;
  border-radius: 12px;
  box-shadow: 0 0 15px rgba(0, 0, 0, 0.1);
}

/* Airline FAQ Section */
.faq {
  max-width: 800px;
  margin: 50px auto;
  padding: 20px;
  background-color: #f9f9f9;
  border-radius: 8px;
  box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1);
}

.faq h2 {
  text-align: center;
  font-size: 24px;
  color: #2c3e50;
  margin-bottom: 30px;
}

.faq-item {
  background: #ffffff;
  border-radius: 6px;
  margin: 15px 0;
  box-shadow: 0 2px 8px rgba(0, 0, 0, 0.1);
  padding: 15px;
}

.faq-item h3 {
  font-size: 18px;
  color: #2276E3;
  margin-bottom: 10px;
  cursor: pointer;
}

.faq-item p {
  font-size: 16px;
  color: #555;
  line-height: 1.6;
}

.faq-item:hover {
  background-color: #eef5fe;
  transition: background-color 0.3s ease;
}

.navbar {
  background-color: #0f1c2e;
  padding: 10px 20px;
  position: sticky;
  top: 0;
  z-index: 1000;
}

.navbar-container {
  display: flex;
  align-items: center;
  justify-content: space-between;
  max-width: 1200px;
  margin: auto;
}

.navbar-logo a {
  color: #fff;
  font-size: 1.5em;
  font-weight: bold;
  text-decoration: none;
}

.navbar-links a {
  color: #ffffff;
  margin-left: 15px;
  text-decoration: none;
  font-size: 1em;
  transition: color 0.3s ease;
}

.navbar-links a:hover {
  color: #f39c12;
}

.navbar-links i {
  margin-right: 5px;
}

body {
  margin: 0;
  font-family: 'Segoe UI', sans-serif;
}

/* Base styles */
.navbar {
  display: flex;
  justify-content: space-between;
  align-items: center;
  background-color: #0d47a1;
  padding: 15px 20px;
  color: white;
  position: relative;
}

.logo {
  font-size: 1.5rem;
  font-weight: bold;
  color: white;
}

.navbar-links {
  display: flex;
  gap: 20px;
  flex-wrap: wrap;
}

.navbar-links a {
  color: white;
  text-decoration: none;
  font-size: 1rem;
  display: flex;
  align-items: center;
  gap: 5px;
  transition: color 0.3s ease;
  position: sticky;
}

.navbar-links a:hover {
  color: #ffcc00;
}

/* Hamburger styles */
.hamburger {
  display: none;
  font-size: 1.5rem;
  cursor: pointer;
  color: white;
}

/* Responsive */
@media (max-width: 768px) {
  .hamburger {
    display: block;
  }

  .navbar-links {
    display: flex;
    flex-direction: column;
    background-color: #1565c0;
    position: absolute;
    top: 60px;
    right: 0;
    width: 100%;
    padding: 10px 0;
    position: sticky;
  }

  .navbar-links.active {
    display: flex;
  }

  .navbar-links a {
    padding: 10px 20px;
    border-top: 1px solid rgba(255, 255, 255, 0.2);
  }
}

#navbar.show {
  display: block;
  /* Makes the navbar visible */
}

.nav-links.active {
  display: flex;
  /* Example: Change this to match your styling */
  flex-direction: column;
  /* Adjust if needed */
  background-color: #f8f9fa;
  /* Optional: Background color for active state */
}

.hamburger.toggle {
  transform: rotate(90deg);
  /* Rotates the hamburger icon */
  transition: transform 0.3s ease;
  /* Smooth transition */
}

.suggestions-box {
  position: absolute;
  background: white;
  border: 1px solid #ccc;
  max-height: 200px;
  overflow-y: auto;
  z-index: 1000;
  width: 100%;
}

.suggestions-box div {
  padding: 10px;
  cursor: pointer;
}

.suggestions-box div:hover {
  background-color: #f0f0f0;
}

.footer {
  background-color: #b14747;
  padding: 20px 40px;
  border-top: 1px solid #ccc;
}

.footer-content {
  display: flex;
  justify-content: space-between;
  align-items: center;
  flex-wrap: wrap;
}

.app-download p {
  margin: 0 0 10px;
  font-size: 16px;
  font-weight: bold;
}

.app-download img {
  height: 40px;
  margin-right: 10px;
}

.payment-logos img {
  height: 30px;
  margin-left: 10px;
}

.flight-status-card {
  background: #001f3f;
  color: white;
  padding: 15px;
  border-radius: 10px;
  font-size: 20px;
  text-align: center;
  width: 80%;
  margin: auto;
  animation: fadeIn 1s ease-in-out;
}

@keyframes fadeIn {
  from {
    opacity: 0;
  }

  to {
    opacity: 1;
  }
}

.live-status-section {
  background-color: #f5f5f5;
  padding: 30px 15px;
  text-align: center;
}

.live-status-section h2 {
  color: #001f3f;
  font-size: 28px;
  margin-bottom: 15px;
}

.flight-ticker {
  overflow: hidden;
  white-space: nowrap;
  width: 100%;
  background-color: #001f3f;
  color: #ffffff;
  font-size: 18px;
  padding: 12px 0;
  position: relative;
  border-radius: 6px;
}

.ticker-content {
  display: inline-block;
  padding-left: 100%;
  animation: scrollLeft 25s linear infinite;
}

@keyframes scrollLeft {
  0% {
    transform: translateX(0%);
  }

  100% {
    transform: translateX(-100%);
  }
}

#statusCard {
  background-color: #fff;
  border-radius: 10px;
  padding: 15px;
  margin: 20px auto;
  width: 80%;
  box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
  font-family: sans-serif;
}

#statusCardStatic,
#flightStatus,
#statusCardLive {
  display: block;
  padding: 10px;
  margin: 10px auto;
  background: #f0f0f0;
  border: 1px solid #ccc;
  font-family: Arial, sans-serif;
}

.navbar {
  position: sticky;
  top: 0;
  background-color: #5b28f4;
  /* or your navbar background */
  z-index: 1000;
  /* Make sure it stays above everything */
}

/* Navbar Links */
.navbar-links {
  display: flex;
  justify-content: space-between;
  align-items: center;
  list-style: none;
  padding: 0;
  margin: 0;
  position: sticky;
}

.navbar-links a {
  text-decoration: none;
  color: #fff;
  font-size: 16px;
  margin: 0 15px;
  display: flex;
  align-items: center;
  transition: color 0.3s ease, transform 0.3s ease;
}

.navbar-links a i {
  margin-right: 8px;
  font-size: 18px;
}

.navbar-links a:hover {
  color: #ff7f50;
  /* Example hover color */
  transform: translateY(-3px);
  /* Slight hover animation */
}

/* Responsive Design */
@media screen and (max-width: 768px) {
  .navbar-links {
    flex-direction: column;
    align-items: flex-start;
    padding: 10px;
  }

  .navbar-links a {
    margin: 10px 0;
  }
}

/* Location Search */
.location-search {
  padding: 30px;
  background: #ffffff;
  margin: 20px;
  border-radius: 12px;
  box-shadow: 0 2px 8px rgba(0, 0, 0, 0.1);
}

.location-search h2 {
  margin-bottom: 15px;
}

#locationInput,
#locationDropdown {
  width: 100%;
  padding: 10px;
  margin: 10px 0;
  font-size: 16px;
}

.body {
  margin: 0;
  padding: 0;
  height: 100%;
  font-family: Arial, sans-serif;
  overflow: hidden;
  /* Prevent scrollbars caused by video */
}

.video-background {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  object-fit: cover;
  /* Just like background-size: cover */
  z-index: -1;
  /* Put it behind the page content */
  background-position: center;
  /* Similar to your image */
  background-repeat: no-repeat;
  /* Not really needed, but keeps the logic */
}

.content {
  position: relative;
  z-index: 1;
  /* Ensure text is above video */
  color: white;
  text-align: center;
  padding-top: 20%;
}
document.addEventListener('DOMContentLoaded', function () {
  // Navbar toggle functionality
  const hamburger = document.getElementById('hamburger');
  const navbarLinks = document.getElementById('navbarLinks');
  if (hamburger && navbarLinks) {
    hamburger.addEventListener('click', () => {
      navbarLinks.classList.toggle('active');
    });
  }

  // Sidebar toggle functionality (if applicable)
  const menuToggle = document.getElementById('menu-toggle');
  const sidebar = document.getElementById('sidebar');
  const closeMenu = document.getElementById('close-menu');
  if (menuToggle && sidebar && closeMenu) {
    menuToggle.addEventListener('click', () => sidebar.classList.add('active'));
    closeMenu.addEventListener('click', () => sidebar.classList.remove('active'));
  }

  // Trip type change visibility for return date
  const tripType = document.querySelectorAll('input[name="trip"]');
  const returnDateGroup = document.getElementById('returnDateGroup');
  tripType.forEach(radio => {
    radio.addEventListener('change', function () {
      if (this.value === 'round-trip' || this.value === 'multi-city') {
        if (returnDateGroup) returnDateGroup.style.display = 'block';
      } else {
        if (returnDateGroup) returnDateGroup.style.display = 'none';
      }
    });
  });

  // Flight booking functionality
  const bookBtn = document.getElementById("bookBtn1");
  if (bookBtn) {
    bookBtn.addEventListener("click", () => {
      const source = document.getElementById("source").value.trim();
      const destination = document.getElementById("destination").value.trim();
      const travellers = document.getElementById("travellers").value;
      const travelClass = document.getElementById("class").value;
      const departureDate = document.getElementById("departureDate").value;

      if (!source || !destination || !departureDate) {
        alert("Please fill out all required fields!");
        return;
      }

      // Save booking details
      localStorage.setItem("source", source);
      localStorage.setItem("destination", destination);
      localStorage.setItem("travellers", travellers);
      localStorage.setItem("travelClass", travelClass);
      localStorage.setItem("departureDate", departureDate);

      // Optional confirmation message before redirection
      alert("Your flight is booked!");

      // Redirect to confirmation page
      window.location.href = "pages/booking_confirmation.html";
    });
  }

  // Search flight functionality
  const searchBtn = document.getElementById("searchBtn1");
  if (searchBtn) {
    searchBtn.addEventListener("click", () => {
      const source = document.getElementById("source").value.trim();
      const destination = document.getElementById("destination").value.trim();
      const departureDate = document.getElementById("departureDate").value;

      if (!source || !destination || !departureDate) {
        alert("Please provide source, destination, and departure date!");
        return;
      }
        
      // Redirect to search results
      const searchUrl = `search_results.html?source=${encodeURIComponent(source)}&destination=${encodeURIComponent(destination)}&departureDate=${encodeURIComponent(departureDate)}`;
      window.location.href = searchUrl;
    });
  }
});
{
    "locations": [
      { "name": "India" },
      { "name": "United Kingdom" },
      { "name": "Thailand" },
      { "name": "Russia" },
      { "name": "Japan" },
      { "name": "Norway" },
      { "name": "Malaysia" }
    ]
  }
  <!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <title>Live Flight Tracker</title>
    <meta name="viewport" content="width=device-width, initial-scale=1.0">

    <!-- Leaflet CSS -->
    <link rel="stylesheet" href="https://unpkg.com/leaflet@1.9.4/dist/leaflet.css" />

    <style>
        body,
        html {
            margin: 0;
            padding: 0;
            height: 100%;
            overflow: hidden;
            font-family: Arial, sans-serif;
        }

        .background {
            position: relative;
            width: 100%;
            height: 100%;
            background: url('https://images.unsplash.com/photo-1518770660439-4636190af475') no-repeat center center/cover;
        }

        .center-text {
            position: absolute;
            top: 20%;
            width: 100%;
            text-align: center;
            color: white;
            font-size: 2rem;
            font-weight: bold;
            text-shadow: 2px 2px 6px #000;
            z-index: 2;
        }

        .map-container {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            opacity: 0.7;
            z-index: 1;
        }

        #map {
            width: 100%;
            height: 100%;
        }

        .bottom-navbar {
            position: absolute;
            bottom: 0;
            width: 100%;
            background-color: #4f00ff;
            color: white;
            display: flex;
            justify-content: space-around;
            align-items: center;
            padding: 10px;
            z-index: 3;
        }

        .nav-item {
            text-align: center;
            font-size: 1rem;
        }

        .nav-item:hover {
            text-decoration: underline;
            cursor: pointer;
        }
    </style>

</head>

<body>
        <div class="map-container">
            <div id="map"></div>
        </div>
    </div>

    <!-- Leaflet JS -->
    <script src="https://unpkg.com/leaflet@1.9.4/dist/leaflet.js"></script>

    <script>
        // Initialize the map
        const map = L.map('map').setView([20.5937, 78.9629], 3); // Centered on India

        // Add OpenStreetMap tiles
        L.tileLayer('https://{s}.tile.openstreetmap.org/{z}/{x}/{y}.png', {
            maxZoom: 19,
            attribution: '© OpenStreetMap'
        }).addTo(map);

        // Create a layer group for planes
        const planesLayer = L.layerGroup().addTo(map);

        // Function to fetch and display planes
        async function fetchPlanes() {
            try {
                const response = await fetch('https://opensky-network.org/api/states/all');
                const data = await response.json();

                planesLayer.clearLayers(); // Clear previous markers

                if (data.states) {
                    data.states.forEach(plane => {
                        const latitude = plane[6];
                        const longitude = plane[5];
                        const callsign = plane[1];

                        if (latitude && longitude) {
                            const marker = L.marker([latitude, longitude], {
                                icon: L.icon({
                                    iconUrl: 'https://img.icons8.com/ios-filled/50/000000/airplane-take-off.png',
                                    iconSize: [30, 30],
                                    iconAnchor: [15, 15]
                                })
                            }).bindPopup(`<b>Flight:</b> ${callsign || "Unknown"}`);
                            planesLayer.addLayer(marker);
                        }
                    });
                }
            } catch (error) {
                console.error('Error fetching plane data:', error);
            }
        }

        // Fetch initially
        fetchPlanes();

        // Update every 10 seconds
        setInterval(fetchPlanes, 10000);
    </script>

</body>

</html>
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <title>Flight Booking</title>
    <style>
        /* Your styling for the booking page */
    </style>
</head>

<body>
    <style>
        /* Body Styling */
        body {
            font-family: 'Poppins', sans-serif;
            background: linear-gradient(to bottom right, #00c6ff, #0072ff);
            height: 100vh;
            margin: 0;
            overflow: hidden;
            display: flex;
            justify-content: center;
            align-items: center;
            position: relative;
        }

        /* Card Styling */
        .card {
            background: #fff;
            padding: 40px 60px;
            border-radius: 25px;
            box-shadow: 0px 15px 45px rgba(0, 0, 0, 0.15);
            text-align: center;
            z-index: 10;
            animation: fadeIn 1s ease-out;
            max-width: 400px;
            width: 100%;
            backdrop-filter: blur(10px);
        }

        /* Checkmark Animation */
        .checkmark {
            width: 100px;
            height: 100px;
            margin: 0 auto 25px;
            border-radius: 50%;
            background: #4CAF50;
            display: flex;
            justify-content: center;
            align-items: center;
            animation: pop 0.6s ease-out;
        }

        /* SVG for Checkmark Icon */
        .checkmark svg {
            width: 60px;
            height: 60px;
            stroke: white;
            stroke-width: 5;
            stroke-linecap: round;
            stroke-linejoin: round;
            fill: none;
            stroke-dasharray: 48;
            stroke-dashoffset: 48;
            animation: draw 0.6s forwards ease;
        }

        /* Heading Style */
        h1 {
            font-size: 2.2em;
            font-weight: 600;
            color: #333;
            margin-bottom: 10px;
            letter-spacing: 0.5px;
        }

        /* Paragraph Text Styling */
        p {
            font-size: 1.2em;
            color: #555;
            margin-bottom: 25px;
            line-height: 1.5;
        }

        /* Button Styling */
        button {
            background: #ff8000;
            color: #fff;
            padding: 12px 30px;
            font-size: 1.1em;
            border: none;
            border-radius: 8px;
            cursor: pointer;
            transition: background 0.3s, transform 0.2s;
            letter-spacing: 1px;
        }

        button:hover {
            background: #e0b794;
            transform: translateY(-2px);
        }

        button:active {
            transform: translateY(0);
        }

        /* Flying Airplane Animation */
        .airplane {
            position: absolute;
            top: 10%;
            left: -80px;
            width: 100px;
            animation: flyAcross 8s linear infinite;
            z-index: 1;
        }

        /* Airplane Flying Keyframe Animation */
        @keyframes flyAcross {
            0% {
                left: -80px;
                transform: rotate(0deg);
            }

            100% {
                left: 110%;
                transform: rotate(10deg);
            }
        }

        /* Animations */
        @keyframes draw {
            to {
                stroke-dashoffset: 0;
            }
        }

        @keyframes pop {
            0% {
                transform: scale(0);
            }

            100% {
                transform: scale(1);
            }
        }

        @keyframes fadeIn {
            from {
                opacity: 0;
            }

            to {
                opacity: 1;
            }
        }
    </style>

    Booking form with source and destination
    <form id="bookingForm">
        <label for="source">Source:</label>
        <input type="text" id="source" name="source" required>
        <label for="destination">Destination:</label>
        <input type="text" id="destination" name="destination" required>
        <button type="submit">Book Flight</button>
    </form>

    <script>
        // Save source and destination to localStorage when the form is submitted
        document.getElementById('bookingForm').addEventListener('submit', function (event) {
            event.preventDefault();

            const source = document.getElementById('source').value;
            const destination = document.getElementById('destination').value;

            // Store source and destination in localStorage
            localStorage.setItem('source', source);
            localStorage.setItem('destination', destination);

            // Redirect to booking confirmation page
            window.location.href = 'booking_confirmation.html';
        });
    </script>

</body>

</html>
/* Global Styles */
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-family: "Segoe UI", sans-serif;
}

/* Global Styles */
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-family: "Segoe UI", sans-serif;
}

body {
    background-color: #f7f9fc;
    color: #333;
    line-height: 1.6;
    padding: 20px;
    background-image: url('https://wallpaperaccess.com/full/1628626.jpg');
    background-size: cover;
    background-repeat: no-repeat;
    background-attachment: fixed;
}

.form-container {
    background-color: #397539;
    padding: 25px;
    border-radius: 10px;
    box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
    max-width: 800px;
    margin: auto;
}

fieldset {
    border: none;
}

legend {
    font-size: 20px;
    font-weight: 600;
    margin-bottom: 10px;
}

.form-content {
    display: flex;
    flex-wrap: wrap;
    gap: 20px;
    align-items: center;
}

.form-group {
    flex: 1 1 250px;
    display: flex;
    flex-direction: column;
}

label {
    margin-bottom: 5px;
    font-weight: 500;
}

input,
select {
    padding: 10px;
    border: 1px solid #ccc;
    border-radius: 8px;
    font-size: 16px;
    margin: 12px;
    transition: 0.3s ease;
}

input:focus,
select:focus {
    border-color: #007bff;
    outline: none;
}

button#searchBtn1 {
    padding: 12px 20px;
    background-color: #e621dc;
    color: #244824;
    border: none;
    border-radius: 8px;
    font-size: 16px;
    cursor: pointer;
    transition: background 0.3s;
    margin-left: 18rem;
    margin-right: 18rem;
}

button#searchBtn1:hover {
    background-color: #0056b3;
}

/* FAQ Section */
.faq-container {
    max-width: 800px;
    margin: 30px auto;
    background-color: #397539;
    border-radius: 10px;
    padding: 25px;
    box-shadow: 0 4px 12px rgba(0, 0, 0, 0.08);
}

.faq-item {
    margin-bottom: 20px;
}

.faq-question {
    font-weight: 600;
    color: #2c3e50;
    cursor: pointer;
    margin-bottom: 5px;
}

.faq-answer {
    padding-left: 10px;
    color: #555;
}

/* Footer Section */
.footer-box {
    background-color: #1f1f1f;
    color: #ccc;
    padding: 50px 20px 30px;
    margin-top: 50px;
    font-size: 15px;
}

.footer-container {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
    gap: 30px;
    max-width: 1200px;
    margin: auto;
}

.footer-column h3 {
    color: #63d485;
    margin-bottom: 15px;
    font-size: 16px;
}

.footer-column ul {
    list-style: none;
}

.footer-column ul li {
    margin-bottom: 10px;
}

.footer-column ul li a {
    text-decoration: none;
    color: #aaa;
    transition: color 0.3s;
}

.footer-column ul li a:hover {
    color: #ffffff;
}

/* Footer Bottom Section */
.last {
    text-align: center;
    margin-top: 40px;
}

.social-icons a {
    display: inline-block;
    color: #ccc;
    margin: 0 10px;
    font-size: 20px;
    transition: color 0.3s;
}

.social-icons a:hover {
    color: #ffffff;
}

.store-icons {
    margin: 15px 0;
}

.store-icons a {
    display: inline-block;
    margin: 10px;
}

.payment-icons {
    margin-top: 20px;
    font-size: 26px;
    color: #aaa;
}

.payment-icons i {
    margin: 0 10px;
    transition: color 0.3s;
}

.payment-icons i:hover {
    color: #fff;
}

.site-footer {
    margin-top: 30px;
    text-align: center;
    font-size: 14px;
    color: #777;
}

hr {
    border: 0;
    border-top: 1px solid #444;
    margin: 30px auto;
    max-width: 90%;
}

/* Responsive */
@media (max-width: 768px) {
    .form-content {
        flex-direction: column;
    }

    .form-group {
        width: 100%;
    }

    .faq-container {
        padding: 20px;
    }

    .footer-container {
        grid-template-columns: 1fr 1fr;
    }
}

@media (max-width: 480px) {
    .footer-container {
        grid-template-columns: 1fr;
        text-align: center;
    }

    .store-icons a img {
        width: 100px;
    }
}

.site-footer {
    background-color: #f4f4f4;
    padding: 40px 20px 20px;
    font-family: Arial, sans-serif;
    font-size: 14px;
    color: #333;
}

.footer-top {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
    gap: 20px;
    border-bottom: 1px solid #ccc;
    padding-bottom: 30px;
}

.footer-column h4 {
    font-weight: bold;
    margin-bottom: 10px;
}

.footer-column ul {
    list-style-type: none;
    padding: 0;
}

.footer-column ul li {
    margin-bottom: 6px;
    cursor: pointer;
}

.footer-bottom {
    display: flex;
    flex-wrap: wrap;
    justify-content: space-between;
    align-items: center;
    padding-top: 20px;
}

.social-icons,
.download-apps,
.payment-icons {
    margin: 10px 0;
}

.social-icons img,
.payment-icons img {
    width: 32px;
    margin-right: 10px;
}

.app-badge {
    height: 40px;
    margin-right: 10px;
}

/* Headings */
h3 {
    text-align: center;
    margin: 30px 0;
    font-size: 24px;
    color: #fb2ad6;
}

/* Form Section */
.form-container {
    background-color: #397539;
    padding: 25px;
    border-radius: 10px;
    box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
    max-width: 800px;
    margin: auto;
}

fieldset {
    border: none;
}

legend {
    font-size: 20px;
    font-weight: 600;
    margin-bottom: 10px;
}

.form-content {
    display: flex;
    flex-wrap: wrap;
    gap: 20px;
    align-items: center;
}

.form-group {
    flex: 1 1 250px;
    display: flex;
    flex-direction: column;
}

label {
    margin-bottom: 5px;
    font-weight: 500;
}

input,
select {
    padding: 10px;
    border: 1px solid #ccc;
    border-radius: 8px;
    font-size: 16px;
    margin: 12px;
    transition: 0.3s ease;
}

input:focus,
select:focus {
    border-color: #007bff;
    outline: none;
}

button#searchBtn1 {
    padding: 12px 20px;
    background-color: #ff0000;
    color: #244824;
    border: none;
    border-radius: 8px;
    font-size: 16px;
    cursor: pointer;
    transition: background 0.3s;
    margin-left: 18rem;
    margin-right: 18rem;
}

button#searchBtn1:hover {
    background-color: #0056b3;
}

/* FAQ Section */
.faq-container {
    max-width: 800px;
    margin: 30px auto;
    background-color: #397539;
    border-radius: 10px;
    padding: 25px;
    box-shadow: 0 4px 12px rgba(0, 0, 0, 0.08);
}

.faq-item {
    margin-bottom: 20px;
}

.faq-question {
    font-weight: 600;
    color: #2c3e50;
    cursor: pointer;
    margin-bottom: 5px;
}

.faq-answer {
    padding-left: 10px;
    color: #efeaea;
}

/* Footer Section */
.footer-box {
    background-color: #1f1f1f;
    color: #ccc;
    padding: 50px 20px 30px;
    margin-top: 50px;
    font-size: 15px;
}

.footer-container {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
    gap: 30px;
    max-width: 1200px;
    margin: auto;
}

.footer-column h3 {
    color: #63d485;
    margin-bottom: 15px;
    font-size: 16px;
}

.footer-column ul {
    list-style: none;
}

.footer-column ul li {
    margin-bottom: 10px;
}

.footer-column ul li a {
    text-decoration: none;
    color: #aaa;
    transition: color 0.3s;
}

.footer-column ul li a:hover {
    color: #ffffff;
}

/* Footer Bottom Section */
.last {
    text-align: center;
    margin-top: 40px;
}

.social-icons a {
    display: inline-block;
    color: #ccc;
    margin: 0 10px;
    font-size: 20px;
    transition: color 0.3s;
}

.social-icons a:hover {
    color: #ffffff;
}

.store-icons {
    margin: 15px 0;
}

.store-icons a {
    display: inline-block;
    margin: 10px;
}

.payment-icons {
    margin-top: 20px;
    font-size: 26px;
    color: #aaa;
}

.payment-icons i {
    margin: 0 10px;
    transition: color 0.3s;
}

.payment-icons i:hover {
    color: #fff;
}

.site-footer {
    margin-top: 30px;
    text-align: center;
    font-size: 14px;
    color: #777;
}

hr {
    border: 0;
    border-top: 1px solid #444;
    margin: 30px auto;
    max-width: 90%;
}

/* Responsive */
@media (max-width: 768px) {
    .form-content {
        flex-direction: column;
    }

    .form-group {
        width: 100%;
    }

    .faq-container {
        padding: 20px;
    }

    .footer-container {
        grid-template-columns: 1fr 1fr;
    }
}

@media (max-width: 480px) {
    .footer-container {
        grid-template-columns: 1fr;
        text-align: center;
    }

    .store-icons a img {
        width: 100px;
    }
}

.site-footer {
    background-color: #f4f4f4;
    padding: 40px 20px 20px;
    font-family: Arial, sans-serif;
    font-size: 14px;
    color: #333;
}

.footer-top {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
    gap: 20px;
    border-bottom: 1px solid #ccc;
    padding-bottom: 30px;
}

.footer-column h4 {
    font-weight: bold;
    margin-bottom: 10px;
}

.footer-column ul {
    list-style-type: none;
    padding: 0;
}

.footer-column ul li {
    margin-bottom: 6px;
    cursor: pointer;
}

.footer-bottom {
    display: flex;
    flex-wrap: wrap;
    align-items: center;
    padding-top: 20px;
}

.social-icons,
.download-apps,
.payment-icons {
    margin: 10px 0;
}

.social-icons img,
.payment-icons img {
    width: 32px;
    margin-right: 10px;
}

.app-badge {
    height: 40px;
    margin-right: 10px;
}

body {
    font-family: Arial, sans-serif;
    margin: 0;
    padding: 20px;
    background-color: #f5f5f5;
}

.form-section {
    margin: 2px 2px;
    padding: 20px;
    background: #fff;
    border: 1px solid #ddd;
    border-radius: 10px;
    box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
}

h2 {
    margin-bottom: 15px;
    font-size: 20px;
    color: #333;
}

/* Container styling */
.form-container-horizontal {
    max-width: 800px;
    margin: 20px auto;
    background-color: #fff;
    padding: 20px;
    border-radius: 10px;
    box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
    border: 1px solid #ddd;
    font-family: Arial, sans-serif;
}

h2 {
    text-align: center;
    margin-bottom: 20px;
    font-size: 18px;
    color: #333;
}

/* Form row styling for horizontal alignment */
/* Styling for the form container */
.form-container-horizontal {
    max-width: 800px;
    margin: 20px auto;
    background-color: #fff;
    padding: 20px;
    border-radius: 10px;
    box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
    border: 1px solid #ddd;
    font-family: Arial, sans-serif;
}

/* Title styling */
h2 {
    text-align: center;
    margin-bottom: 20px;
    font-size: 18px;
    color: #333;
}

/* Form row for horizontal alignment */
.form-row {
    display: flex;
    justify-content: space-between;
    /* Ensures even spacing between elements */
    align-items: center;
    /* Aligns elements vertically */
    gap: 15px;
    /* Space between input fields and button */
    flex-wrap: wrap;
    /* Adjusts layout for smaller screens */
}

/* Individual form group styling */
.form-group {
    flex: 1;
    /* Makes fields flexible for proper alignment */
    min-width: 200px;
    /* Minimum width to ensure visibility */
}

label {
    display: block;
    font-weight: bold;
    margin-bottom: 5px;
    color: #333;
}

input[type="text"],
input[type="date"],
select {
    width: 100%;
    padding: 8px;
    font-size: 14px;
    border: 1px solid #ccc;
    border-radius: 5px;
    box-sizing: border-box;
}

/* Styling for the dropdown (train class) */
select {
    background-color: #f9f9f9;
}

/* Button styling */
button {
    flex: 0 1 auto;
    /* Adjusts button size without affecting fields */
    padding: 12px 20px;
    background-color: #007BFF;
    color: #fff;
    border: none;
    border-radius: 5px;
    cursor: pointer;
    font-size: 16px;
    transition: background-color 0.3s ease;
}

button:hover {
    background-color: #0056b3;
}

/* Responsive adjustments */
@media (max-width: 768px) {
    .form-row {
        flex-direction: column;
        /* Stacks fields vertically on smaller screens */
    }

    button {
        width: 100%;
        /* Makes the button full width on small screens */
    }
}
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Airline Reservation System - Train Ticket Booking</title>
    <link rel="stylesheet" href="Common.css">
    <link rel="stylesheet" href="Bus.css">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.0/css/all.min.css" />
    <script src="Bus.js"></script>
</head>

<body>
    <div class="form-container-horizontal">
        <h2>Bus Ticket Booking</h2>
        <form id="busSearchForm">
            <input type="text" id="busSourceInput" placeholder="Enter source location">
            <input type="text" id="busDestinationInput" placeholder="Enter destination location">
            <input type="date" id="busDateInput">
            <select id="busClass">
                <option value="Sleeper">Sleeper</option>
                <option value="Semi-Sleeper">Semi-Sleeper</option>
            </select>
            <button type="submit">Search Bus</button>
        </form>
        <div id="busResults"></div>


        </fieldset>
        </form>

        <!-- Results Placeholder -->
        <div id="trainResults"></div>
    </div>

    <!-- FAQs Section -->
    <h3>Bus Booking FAQs</h3>
    <div class="faq-container">
        <div class="faq-item">
            <div class="faq-question">What are the advantages of booking bus tickets online?</div>
            <div class="faq-answer">
                Online bus booking lets you compare operators, select seats, view bus types, and pay securely—all from
                your home or mobile device.
            </div>
        </div>
        <div class="faq-item">
            <div class="faq-question">When should I book bus tickets for the best availability?</div>
            <div class="faq-answer">
                It's recommended to book bus tickets 2–3 days in advance, especially during weekends, holidays, or peak
                seasons, to ensure seat availability.
            </div>
        </div>
        <div class="faq-item">
            <div class="faq-question">How can I book bus tickets online?</div>
            <div class="faq-answer">
                Enter your source, destination, and travel date on a bus booking platform, choose your bus and seat, and
                confirm the booking by making payment.
            </div>
        </div>
        <div class="faq-item">
            <div class="faq-question">What documents are required for bus travel?</div>
            <div class="faq-answer">
                While booking, no documents are needed. At the time of boarding, carry a valid photo ID and the e-ticket
                (SMS or printout) provided by the booking platform.
            </div>
        </div>
        <div class="faq-item">
            <div class="faq-question">Why book bus tickets online through Goibibo?</div>
            <div class="faq-answer">
                Goibibo offers a seamless booking process, multiple operator options, exclusive discounts, GoCash
                rewards, and various payment methods.
            </div>
        </div>
        <div class="faq-item">
            <div class="faq-question">What additional services does Goibibo provide for bus travelers?</div>
            <div class="faq-answer">
                Goibibo allows you to view bus photos, track live bus location, check boarding points, and easily cancel
                or reschedule your tickets.
            </div>
        </div>
    </div>

    <!-- Footer Section -->
    <footer class="site-footer">
        <div class="footer-top">
            <div class="footer-column">
                <h4>OUR PRODUCTS</h4>
                <ul>
                    <li>Domestic Hotels</li>
                    <li>International Hotels</li>
                    <li>International Flights</li>
                    <li>Bus Booking</li>
                    <li>Cab Booking</li>
                    <li>Train Ticket Booking</li>
                    <li>Route Planner</li>
                    <li>Cheap Flights</li>
                    <li>Hotels near me</li>
                    <li>Popular Airlines</li>
                </ul>
            </div>
            <div class="footer-column">
                <h4>COMPANY</h4>
                <ul>
                    <li>About Us</li>
                    <li>Privacy</li>
                    <li>Careers</li>
                    <li>Customer Support</li>
                    <li>FAQs</li>
                </ul>
            </div>
            <div class="footer-column">
                <h4>TRENDING HOTEL CITIES</h4>
                <ul>
                    <li>Hotels in Goa</li>
                    <li>Hotels in Delhi</li>
                    <li>Hotels in Mumbai</li>
                    <li>Hotels in Bangalore</li>
                    <li>Hotels in Chennai</li>
                </ul>
            </div>
            <div class="footer-column">
                <h4>TRENDING INTERNATIONAL HOTEL CITIES</h4>
                <ul>
                    <li>Hotels in Dubai</li>
                    <li>Hotels in Singapore</li>
                    <li>Hotels in London</li>
                    <li>Hotels in New York</li>
                    <li>Hotels in Paris</li>
                </ul>
            </div>
            <div class="footer-column">
                <h4>TOP SEARCHED HOTELS BY AREA</h4>
                <ul>
                    <li>Hotels in Panchgani</li>
                    <li>Hotels in Shirdi</li>
                    <li>Hotels in Ooty</li>
                    <li>Hotels in Manali</li>
                    <li>Hotels in Lonavala</li>
                </ul>
            </div>
            <div class="footer-column">
                <h4>ALTERNATE ACCOMMODATION IN CITY</h4>
                <ul>
                    <li>Homestays in Coorg</li>
                    <li>Homestays in Ooty</li>
                    <li>Homestays in Manali</li>
                    <li>Villas in Goa</li>
                    <li>Villas in Lonavala</li>
                </ul>
            </div>
            <div class="footer-column">
                <h4>TOP 5 STAR HOTEL CITIES</h4>
                <ul>
                    <li>5 Star Hotels in Delhi</li>
                    <li>5 Star Hotels in Mumbai</li>
                    <li>5 Star Hotels in Goa</li>
                    <li>5 Star Hotels in Chennai</li>
                    <li>5 Star Hotels in Kolkata</li>
                </ul>
            </div>
        </div>

        <div class="footer-bottom">
            <div class="social-icons">
                <span>Follow Us</span>
                <a href="#"><img src="https://img.icons8.com/ios-filled/24/facebook--v1.png" /></a>
                <a href="#"><img src="https://img.icons8.com/ios-filled/24/twitter--v1.png" /></a>
                <a href="#"><img src="https://img.icons8.com/ios-filled/24/instagram-new.png" /></a>
            </div>
            <div class="download-apps">
                <span>Download our Mobile Apps</span>
                <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/7/78/Google_Play_Store_badge_EN.svg/2560px-Google_Play_Store_badge_EN.svg.png"
                    alt="Play Store" class="app-badge" />
                <img src="https://developer.apple.com/assets/elements/badges/download-on-the-app-store.svg"
                    alt="App Store" class="app-badge" />
            </div>
            <div class="payment-icons">
                <img src="https://img.icons8.com/color/48/visa.png" />
                <img src="https://img.icons8.com/color/48/mastercard-logo.png" />
                <img src="https://img.icons8.com/color/48/rupay.png" />
                <img src="https://img.icons8.com/color/48/paypal.png" />
            </div>
        </div>
    </footer>
</body>


</html>
document.addEventListener("DOMContentLoaded", function () {
    console.log("Bus.js script loaded successfully!"); // Debugging confirmation

    const form = document.getElementById("busSearchForm"); // Access the form element
    const resultsContainer = document.getElementById("busResults"); // Results container

    if (form && resultsContainer) {
        // Event listener for the bus search form submission
        form.addEventListener("submit", function (e) {
            e.preventDefault(); // Prevent default form submission
            console.log("Form submission event triggered");

            // Retrieve values from form fields
            const source = document.getElementById("busSourceInput").value.trim();
            const destination = document.getElementById("busDestinationInput").value.trim();
            const date = document.getElementById("busDateInput").value.trim();
            const busClass = document.getElementById("busClass").value.trim();

            // Validate inputs
            if (!source || !destination || !date || !busClass) {
                alert("Please fill in all required fields before searching.");
                return; // Exit if validation fails
            }

            // Simulate search results (mock data)
            const mockData = `
                <h4>Available Buses</h4>
                <ul class="bus-list">
                    <li><strong>Bus 1:</strong> ${source} to ${destination} | ${date} | ${busClass.toUpperCase()}</li>
                    <li><strong>Bus 2:</strong> ${source} to ${destination} | ${date} | ${busClass.toUpperCase()}</li>
                </ul>
            `;
            resultsContainer.innerHTML = mockData; // Inject search results into the DOM
            console.log("Search results displayed successfully!"); // Debugging confirmation
        });
    } else {
        console.error("The form with ID 'busSearchForm' or the results container was not found."); // Error logging
    }
});
/* Global Styles */
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-family: "Segoe UI", sans-serif;
}


body {
    background-color: #1e498b;
    color: #333;
    line-height: 1.6;
    padding: 20px;
    background-image: url('https://wallpaperaccess.com/full/2428190.jpg');
    background-size: cover;
    background-repeat: no-repeat;
    background-position: center center;
    position: relative;
    z-index: 0;
}

/* Add an overlay to sharpen the visual effect */
body::before {
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    background-image: inherit;
    filter: blur(0px) brightness(0.8);
    z-index: -1;
}


/* Headings */
h3 {
    text-align: center;
    margin: 30px 0;
    font-size: 24px;
    color: #e5e9ed;
}

/* Form Section */
.form-container {
    /* background-color: #397539; */
    padding: 25px;
    border-radius: 10px;
    box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
    max-width: 800px;
    margin: auto;
}

fieldset {
    border: none;
}

legend {
    font-size: 20px;
    font-weight: 600;
    margin-bottom: 10px;
}

.form-content {
    display: flex;
    flex-wrap: wrap;
    gap: 20px;
    align-items: center;
}

.form-group {
    flex: 1 1 250px;
    display: flex;
    flex-direction: column;
}

label {
    margin-bottom: 5px;
    font-weight: 500;
}

input,
select {
    padding: 10px;
    border: 1px solid #ccc;
    border-radius: 8px;
    font-size: 16px;
    margin: 12px;
    transition: 0.3s ease;
}

input:focus,
select:focus {
    border-color: #007bff;
    outline: none;
}

button#searchBtn1 {
    padding: 12px 20px;
    background-color: #ff0000;
    color: #244824;
    border: none;
    border-radius: 8px;
    font-size: 16px;
    cursor: pointer;
    transition: background 0.3s;
    margin-left: 18rem;
    margin-right: 18rem;
}

button#searchBtn1:hover {
    background-color: #0056b3;
}

/* FAQ Section */
.faq-container {
    max-width: 800px;
    margin: 30px auto;
    background-color: #397539;
    border-radius: 10px;
    padding: 25px;
    box-shadow: 0 4px 12px rgba(0, 0, 0, 0.08);
}

.faq-item {
    margin-bottom: 20px;
}

.faq-question {
    font-weight: 600;
    color: #2c3e50;
    cursor: pointer;
    margin-bottom: 5px;
}

.faq-answer {
    padding-left: 10px;
    color: #f1e9e9;
}

/* Footer Section */
.footer-box {
    background-color: #1f1f1f;
    color: #ccc;
    padding: 50px 20px 30px;
    margin-top: 50px;
    font-size: 15px;
}

.footer-container {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
    gap: 30px;
    max-width: 1200px;
    margin: auto;
}

.footer-column h3 {
    color: #63d485;
    margin-bottom: 15px;
    font-size: 16px;
}

.footer-column ul {
    list-style: none;
    padding: 0;
}

.footer-column ul li {
    margin-bottom: 10px;
}

.footer-column ul li a {
    text-decoration: none;
    color: #aaa;
    transition: color 0.3s;
}

.footer-column ul li a:hover {
    color: #ffffff;
}

.last {
    text-align: center;
    margin-top: 40px;
}

.social-icons a {
    display: inline-block;
    color: #ccc;
    margin: 0 10px;
    font-size: 20px;
    transition: color 0.3s;
}

.social-icons a:hover {
    color: #ffffff;
}

.store-icons {
    margin: 15px 0;
}

.store-icons a {
    display: inline-block;
    margin: 10px;
}

.payment-icons {
    margin-top: 20px;
    font-size: 26px;
    color: #aaa;
}

.payment-icons i {
    margin: 0 10px;
    transition: color 0.3s;
}

.payment-icons i:hover {
    color: #fff;
}

.site-footer {
    background-color: #f4f4f4;
    padding: 40px 20px 20px;
    text-align: center;
    font-family: Arial, sans-serif;
    font-size: 14px;
    color: #333;
}

.footer-top {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
    gap: 20px;
    border-bottom: 1px solid #ccc;
    padding-bottom: 30px;
}

.footer-column h4 {
    font-weight: bold;
    margin-bottom: 10px;
}

.footer-bottom {
    display: flex;
    flex-wrap: wrap;
    justify-content: space-between;
    align-items: center;
    padding-top: 20px;
}

.social-icons img,
.payment-icons img {
    width: 32px;
    margin-right: 10px;
}

.app-badge {
    height: 40px;
    margin-right: 10px;
}

hr {
    border: 0;
    border-top: 1px solid #444;
    margin: 30px auto;
    max-width: 90%;
}

/* Responsive */
@media (max-width: 768px) {
    .form-content {
        flex-direction: column;
    }

    .form-group {
        width: 100%;
    }

    .faq-container {
        padding: 20px;
    }

    .footer-container {
        grid-template-columns: 1fr 1fr;
    }
}

@media (max-width: 480px) {
    .footer-container {
        grid-template-columns: 1fr;
        text-align: center;
    }

    .store-icons a img {
        width: 100px;
    }
}
body {
    font-family: Arial, sans-serif;
    margin: 0;
    padding: 20px;
    background-color: #f5f5f5;
}

.form-section {
    margin: 20px 0;
    padding: 20px;
    background: #fff;
    border: 1px solid #ddd;
    border-radius: 10px;
    box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
}

h2 {
    margin-bottom: 15px;
    font-size: 20px;
    color: #333;
}

label {
    display: block;
    font-weight: bold;
    margin-bottom: 5px;
    color: #333;
}

input[type="text"],
input[type="date"] {
    width: 100%;
    padding: 8px;
    margin-bottom: 15px;
    border: 1px solid #ccc;
    border-radius: 5px;
    box-sizing: border-box;
}


/* Form row styling for horizontal alignment */
/* Styling for the form container */
.form-container-horizontal {
    max-width: 800px;
    margin: 20px auto;
    background-color: #fff;
    padding: 20px;
    border-radius: 10px;
    box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
    border: 1px solid #ddd;
    font-family: Arial, sans-serif;
}

/* Title styling */
h2 {
    text-align: center;
    margin-bottom: 20px;
    font-size: 18px;
    color: #333;
}

/* Form row for horizontal alignment */
.form-row {
    display: flex;
    justify-content: space-between;
    /* Ensures even spacing between elements */
    align-items: center;
    /* Aligns elements vertically */
    gap: 15px;
    /* Space between input fields and button */
    flex-wrap: wrap;
    /* Adjusts layout for smaller screens */
}

/* Individual form group styling */
.form-group {
    flex: 1;
    /* Makes fields flexible for proper alignment */
    min-width: 200px;
    /* Minimum width to ensure visibility */
}

label {
    display: block;
    font-weight: bold;
    margin-bottom: 5px;
    color: #333;
}

input[type="text"],
input[type="date"],
select {
    width: 100%;
    padding: 8px;
    font-size: 14px;
    border: 1px solid #ccc;
    border-radius: 5px;
    box-sizing: border-box;
}

/* Styling for the dropdown (train class) */
select {
    background-color: #f9f9f9;
}

/* Button styling */
button {
    flex: 0 1 auto;
    /* Adjusts button size without affecting fields */
    padding: 12px 20px;
    background-color: #007BFF;
    color: #fff;
    border: none;
    border-radius: 5px;
    cursor: pointer;
    font-size: 16px;
    transition: background-color 0.3s ease;
}

button:hover {
    background-color: #0056b3;
}

/* Responsive adjustments */
@media (max-width: 768px) {
    .form-row {
        flex-direction: column;
        /* Stacks fields vertically on smaller screens */
    }

    button {
        width: 100%;
        /* Makes the button full width on small screens */
    }
}
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Airline Reservation System - Train Ticket Booking</title>
    <script src="Cabs.js"></script>
    <link rel="stylesheet" href="Common.css">
    <link rel="stylesheet" href="Cabs.css">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.0/css/all.min.css" />
</head>

<body>
    <h3>Book Cabs</h3>
    <div class="form-container">
        <div class="form-container-horizontal">
            <h2>Cab Booking</h2>
            <div class="form-row">
                <div class="form-group">
                    <label for="trainSourceInput">From:</label>
                    <input type="text" id="trainSourceInput" placeholder="Enter source station">
                </div>
                <div class="form-group">
                    <label for="trainDestinationInput">To:</label>
                    <input type="text" id="trainDestinationInput" placeholder="Enter destination station">
                </div>
                <div class="form-group">
                    <label for="trainDateInput">Date:</label>
                    <input type="date" id="trainDateInput">
                </div>
                <div class="form-group">
                    <label for="traintimeInput">Time:</label>
                    <input type="time" id="traintimeInput">
                </div>
                <button id="trainSearchButton">Search Cabs</button>
            </div>
        </div>

        </fieldset>
        </form>

        <!-- Results Placeholder -->
        <div id="trainResults"></div>
    </div>

    <!-- FAQs Section -->
    <h3>Cab Booking FAQs</h3>
    <div class="faq-container">
        <div class="faq-item">
            <div class="faq-question">What are the advantages of booking cabs online?</div>
            <div class="faq-answer">
                Online cab booking offers convenience, real-time tracking, multiple cab options, secure payments, and
                doorstep pickup.
            </div>
        </div>
        <div class="faq-item">
            <div class="faq-question">When should I book a cab for outstation travel?</div>
            <div class="faq-answer">
                It's ideal to book outstation cabs at least 24 hours in advance to ensure availability and better
                pricing, especially during weekends or holidays.
            </div>
        </div>
        <div class="faq-item">
            <div class="faq-question">How can I book a cab online?</div>
            <div class="faq-answer">
                You can book a cab by selecting your pickup and drop-off location on a cab service app or website,
                choosing your cab type, and confirming your booking with payment.
            </div>
        </div>
        <div class="faq-item">
            <div class="faq-question">What documents are required to book a cab?</div>
            <div class="faq-answer">
                No documents are required at the time of booking. However, carrying a valid ID during the ride is
                recommended, especially for intercity travel.
            </div>
        </div>
        <div class="faq-item">
            <div class="faq-question">Why book cabs through Goibibo?</div>
            <div class="faq-answer">
                Goibibo offers competitive pricing, reliable drivers, a wide range of cab options, GoCash discounts, and
                secure payment methods.
            </div>
        </div>
        <div class="faq-item">
            <div class="faq-question">What additional cab services does Goibibo provide?</div>
            <div class="faq-answer">
                Goibibo offers one-way, round trip, airport transfers, outstation, and local city rides, along with
                options to schedule a cab in advance.
            </div>
        </div>
    </div>
    <!-- Footer Section -->
    <footer class="site-footer">
        <div class="footer-top">
            <div class="footer-column">
                <h4>OUR PRODUCTS</h4>
                <ul>
                    <li>Domestic Hotels</li>
                    <li>International Hotels</li>
                    <li>International Flights</li>
                    <li>Bus Booking</li>
                    <li>Cab Booking</li>
                    <li>Train Ticket Booking</li>
                    <li>Route Planner</li>
                    <li>Cheap Flights</li>
                    <li>Hotels near me</li>
                    <li>Popular Airlines</li>
                </ul>
            </div>
            <div class="footer-column">
                <h4>COMPANY</h4>
                <ul>
                    <li>About Us</li>
                    <li>Privacy</li>
                    <li>Careers</li>
                    <li>Customer Support</li>
                    <li>FAQs</li>
                </ul>
            </div>
            <div class="footer-column">
                <h4>TRENDING HOTEL CITIES</h4>
                <ul>
                    <li>Hotels in Goa</li>
                    <li>Hotels in Delhi</li>
                    <li>Hotels in Mumbai</li>
                    <li>Hotels in Bangalore</li>
                    <li>Hotels in Chennai</li>
                </ul>
            </div>
            <div class="footer-column">
                <h4>TRENDING INTERNATIONAL HOTEL CITIES</h4>
                <ul>
                    <li>Hotels in Dubai</li>
                    <li>Hotels in Singapore</li>
                    <li>Hotels in London</li>
                    <li>Hotels in New York</li>
                    <li>Hotels in Paris</li>
                </ul>
            </div>
            <div class="footer-column">
                <h4>TOP SEARCHED HOTELS BY AREA</h4>
                <ul>
                    <li>Hotels in Panchgani</li>
                    <li>Hotels in Shirdi</li>
                    <li>Hotels in Ooty</li>
                    <li>Hotels in Manali</li>
                    <li>Hotels in Lonavala</li>
                </ul>
            </div>
            <div class="footer-column">
                <h4>ALTERNATE ACCOMMODATION IN CITY</h4>
                <ul>
                    <li>Homestays in Coorg</li>
                    <li>Homestays in Ooty</li>
                    <li>Homestays in Manali</li>
                    <li>Villas in Goa</li>
                    <li>Villas in Lonavala</li>
                </ul>
            </div>
            <div class="footer-column">
                <h4>TOP 5 STAR HOTEL CITIES</h4>
                <ul>
                    <li>5 Star Hotels in Delhi</li>
                    <li>5 Star Hotels in Mumbai</li>
                    <li>5 Star Hotels in Goa</li>
                    <li>5 Star Hotels in Chennai</li>
                    <li>5 Star Hotels in Kolkata</li>
                </ul>
            </div>
        </div>

        <div class="footer-bottom">
            <div class="social-icons">
                <a target="_blank" href="http://www.facebook.com/goibibo" title="Facebook" aria-label="Facebook">
                    <span class="footer-sprite facebookIcon"></span>
                </a>
                <a target="_blank" href="http://twitter.com/goibibo" title="Twitter" aria-label="Twitter">
                    <span class="footer-sprite twitterIcon"></span>
                </a>
                <a target="_blank" href="https://plus.google.com/+goibibo/" title="Google Plus"
                    aria-label="Google Plus">
                    <span class="footer-sprite gplusIcon"></span>
                </a>
                <a target="_blank" href="http://www.youtube.com/user/goibibo" title="YouTube" aria-label="YouTube">
                    <span class="footer-sprite youtubeIcon"></span>
                </a>
            </div>
            <div class="download-apps">
                <span>Download our Mobile Apps</span>
                <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/7/78/Google_Play_Store_badge_EN.svg/2560px-Google_Play_Store_badge_EN.svg.png"
                    alt="Play Store" class="app-badge" />
                <img src="https://developer.apple.com/assets/elements/badges/download-on-the-app-store.svg"
                    alt="App Store" class="app-badge" />
            </div>
            <div class="payment-icons">
                <img src="https://img.icons8.com/color/48/visa.png" />
                <img src="https://img.icons8.com/color/48/mastercard-logo.png" />
                <img src="https://img.icons8.com/color/48/rupay.png" />
                <img src="https://img.icons8.com/color/48/paypal.png" />
            </div>
        </div>
    </footer>
</body>

</html>
document.addEventListener("DOMContentLoaded", function () {
    // Event listener for the cab search button
    const searchButton = document.querySelector("#trainSearchButton");
    searchButton.addEventListener("click", function () {
        // Get input values
        const pickupLocation = document.querySelector("#trainSourceInput").value.trim();
        const dropLocation = document.querySelector("#trainDestinationInput").value.trim();
        const date = document.querySelector("#trainDateInput").value.trim();
        const time = document.querySelector("#traintimeInput").value.trim();

        // Validation for empty fields
        if (!pickupLocation || !dropLocation || !date || !time) {
            alert("Please fill in all required fields before searching.");
            return;
        }

        // Example alert for search results (replace with actual functionality)
        alert(`Searching cabs from ${pickupLocation} to ${dropLocation} on ${date} at ${time}`);
    });
});
body {
    font-family: Arial, sans-serif;
    margin: 0;
    padding: 20px;
    background-color: #f5f5f5;
    background-image: url('https://th.bing.com/th/id/OIP.mke_rycWCHTeF_nNjDTJ9QHaE7?rs=1&pid=ImgDetMain');
}

.form {
    max-width: 500px;
    margin: 0 auto;
    background-color: #fff;
    padding: 20px;
    border: 1px solid #ddd;
    border-radius: 10px;
    box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
}

div {
    margin-bottom: 20px;
    /* Spacing between each field */
}

label {
    display: block;
    font-weight: bold;
    margin-bottom: 8px;
    color: #333;
}

input[type="text"],
input[type="date"],
input[type="number"],
select {
    width: 100%;
    padding: 10px;
    border: 1px solid #ccc;
    border-radius: 5px;
    box-sizing: border-box;
    font-size: 14px;
    cursor: pointer;
}

input[type="text"]:focus,
input[type="date"]:focus,
input[type="number"]:focus,
select:focus {
    border-color: #007BFF;
    outline: none;
}

button {
    background-color: #007BFF;
    color: white;
    border: none;
    padding: 12px 20px;
    border-radius: 5px;
    cursor: pointer;
    font-size: 16px;
    width: 100%;
    transition: background-color 0.3s ease;
}

button:hover {
    background-color: #0056b3;
}

/* Additional spacing for better layout on mobile */
@media (max-width: 768px) {
    form {
        padding: 15px;
    }

    input[type="text"],
    input[type="date"],
    input[type="number"],
    select {
        font-size: 12px;
    }

    button {
        font-size: 14px;
        padding: 10px 16px;
    }
}



/* Headings */
h3 {
    text-align: center;
    margin: 30px 0;
    font-size: 24px;
    color: #ff1010;
}

/* Form Section */
.form-container {
    /* background-color: #397539; */
    background-color: white;
    padding: 25px;
    border-radius: 10px;
    box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
    /* max-width: 800px; */
    margin: auto;
}

fieldset {
    border: none;
}

legend {
    font-size: 20px;
    font-weight: 600;
    margin-bottom: 10px;
}

.form-content {
    display: flex;
    flex-wrap: wrap;
    gap: 20px;
    align-items: center;
}

.form-group {
    flex: 1 1 250px;
    display: flex;
    flex-direction: column;
}

label {
    margin-bottom: 5px;
    font-weight: 500;
}

input,
select {
    padding: 10px;
    border: 1px solid #ccc;
    border-radius: 8px;
    font-size: 16px;
    transition: 0.3s ease;
}

input:focus,
select:focus {
    border-color: #007bff;
    outline: none;
}

/* Basic styling for the container */
body {
    font-family: Arial, sans-serif;
    margin: 0;
    padding: 0;
    background-color: #f5f5f5;
}

div {
    margin-bottom: 15px;
    padding: 10px;
}

label {
    display: block;
    font-weight: bold;
    margin-bottom: 5px;
    color: #333;
}

input[type="text"],
input[type="date"],
input[type="number"] {
    width: 100%;
    padding: 8px;
    margin-top: 3px;
    border: 1px solid #ccc;
    border-radius: 5px;
    box-sizing: border-box;
    cursor: pointer;
}

/* Styling for the button */
#searchButton {
    background-color: #007BFF;
    color: white;
    border: none;
    padding: 10px 20px;
    border-radius: 5px;
    cursor: pointer;
    font-size: 16px;
    transition: background-color 0.3s ease;
}

#searchButton:hover {
    background-color: #0056b3;
}

/* Add a responsive layout */
@media (max-width: 768px) {

    input[type="text"],
    input[type="date"],
    input[type="number"] {
        font-size: 14px;
    }

    #searchButton {
        font-size: 14px;
        padding: 8px 16px;
    }
}


/* FAQ Section */
.faq-container {
    /* max-width: 800px; */
    margin: 30px auto;
    /* background-color: #397539; */
    border-radius: 10px;
    padding: 25px;
    box-shadow: 0 4px 12px rgba(0, 0, 0, 0.08);
}

.faq-item {
    margin-bottom: 20px;
}

.faq-question {
    font-weight: 600;
    color: #2c3e50;
    cursor: pointer;
    margin-bottom: 5px;
}

.faq-answer {
    padding-left: 10px;
    color: #f1e9e9;
}

/* Footer Section */
.footer-box {
    background-color: #1f1f1f;
    color: #ccc;
    padding: 50px 20px 30px;
    margin-top: 50px;
    font-size: 15px;
}

.footer-container {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
    gap: 30px;
    max-width: 1200px;
    margin: auto;
}

.footer-column h3 {
    color: #63d485;
    margin-bottom: 15px;
    font-size: 16px;
}

.footer-column ul {
    list-style: none;
}

.footer-column ul li {
    margin-bottom: 10px;
}

.footer-column ul li a {
    text-decoration: none;
    color: #aaa;
    transition: color 0.3s;
}

.footer-column ul li a:hover {
    color: #ffffff;
}

/* Footer Bottom Section */
.last {
    text-align: center;
    margin-top: 40px;
}

.social-icons a {
    display: inline-block;
    color: #ccc;
    margin: 0 10px;
    font-size: 20px;
    transition: color 0.3s;
}

.social-icons a:hover {
    color: #ffffff;
}

.store-icons {
    margin: 15px 0;
}

.store-icons a {
    display: inline-block;
    margin: 10px;
}

.payment-icons {
    margin-top: 20px;
    font-size: 26px;
    color: #aaa;
}

.payment-icons i {
    margin: 0 10px;
    transition: color 0.3s;
}

.payment-icons i:hover {
    color: #fff;
}

.site-footer {
    margin-top: 30px;
    text-align: center;
    font-size: 14px;
    color: #777;
}

hr {
    border: 0;
    border-top: 1px solid #444;
    margin: 30px auto;
    max-width: 90%;
}

/* Responsive */
@media (max-width: 768px) {
    .form-content {
        flex-direction: column;
    }

    .form-group {
        width: 100%;
    }

    .faq-container {
        padding: 20px;
    }

    .footer-container {
        grid-template-columns: 1fr 1fr;
    }
}

@media (max-width: 480px) {
    .footer-container {
        grid-template-columns: 1fr;
        text-align: center;
    }

    .store-icons a img {
        width: 100px;
    }
}

.site-footer {
    background-color: #f4f4f4;
    padding: 40px 20px 20px;
    font-family: Arial, sans-serif;
    font-size: 14px;
    color: #333;
}

.footer-top {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
    gap: 20px;
    border-bottom: 1px solid #ccc;
    padding-bottom: 30px;
}

.footer-column h4 {
    font-weight: bold;
    margin-bottom: 10px;
}

.footer-column ul {
    list-style-type: none;
    padding: 0;
}

.footer-column ul li {
    margin-bottom: 6px;
    cursor: pointer;
}

.footer-bottom {
    display: flex;
    flex-wrap: wrap;
    justify-content: space-between;
    align-items: center;
    padding-top: 20px;
}

.social-icons,
.download-apps,
.payment-icons {
    margin: 10px 0;
}

.social-icons img,
.payment-icons img {
    width: 32px;
    margin-right: 10px;
}

.app-badge {
    height: 40px;
    margin-right: 10px;
}
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>AI Country Search</title>
    <style>
        body {
            background-color: rgb(167, 217, 253);
            font-family: Arial, sans-serif;
            padding: 2rem;
        }

        #letter-buttons button {
            margin: 2px;
            padding: 5px 10px;
        }

        #countryList {
            margin-top: 1rem;
        }

        input,
        button {
            padding: 8px;
            margin-top: 10px;
        }
    </style>
</head>

<body>
    <h2>AI-Powered Country Search</h2>

    <div id="letter-buttons"></div>

    <input type="text" id="searchBox" placeholder="Search country (try typing 'countries with A')" />
    <button onclick="voiceSearch()">🎤 Speak</button>

    <ul id="countryList"></ul>

    <script src="https://cdn.jsdelivr.net/npm/fuse.js@6.6.2"></script>
    <script>
        const countries = [/* all 195 countries alphabetically */ "Afghanistan", "Albania", "Algeria", "Andorra", "Angola", "Argentina", "Armenia", "Australia", "Austria", "Azerbaijan",
            "Bahamas", "Bahrain", "Bangladesh", "Barbados", "Belarus", "Belgium", "Belize", "Benin", "Bhutan", "Bolivia",
            "Bosnia and Herzegovina", "Botswana", "Brazil", "Brunei", "Bulgaria", "Burkina Faso", "Burundi",
            "Cabo Verde", "Cambodia", "Cameroon", "Canada", "Central African Republic", "Chad", "Chile", "China", "Colombia", "Comoros", "Congo", "Costa Rica", "Croatia", "Cuba", "Cyprus", "Czech Republic",
            "Denmark", "Djibouti", "Dominica", "Dominican Republic",
            "Ecuador", "Egypt", "El Salvador", "Equatorial Guinea", "Eritrea", "Estonia", "Eswatini", "Ethiopia",
            "Fiji", "Finland", "France",
            "Gabon", "Gambia", "Georgia", "Germany", "Ghana", "Greece", "Grenada", "Guatemala", "Guinea", "Guyana",
            "Haiti", "Honduras", "Hungary",
            "Iceland", "India", "Indonesia", "Iran", "Iraq", "Ireland", "Israel", "Italy",
            "Jamaica", "Japan", "Jordan",
            "Kazakhstan", "Kenya", "Kiribati", "Kuwait", "Kyrgyzstan",
            "Laos", "Latvia", "Lebanon", "Lesotho", "Liberia", "Libya", "Liechtenstein", "Lithuania", "Luxembourg",
            "Madagascar", "Malawi", "Malaysia", "Maldives", "Mali", "Malta", "Mauritania", "Mauritius", "Mexico", "Micronesia", "Moldova", "Monaco", "Mongolia", "Montenegro", "Morocco", "Mozambique", "Myanmar",
            "Namibia", "Nauru", "Nepal", "Netherlands", "New Zealand", "Nicaragua", "Niger", "Nigeria", "North Korea", "North Macedonia", "Norway",
            "Oman",
            "Pakistan", "Palau", "Panama", "Papua New Guinea", "Paraguay", "Peru", "Philippines", "Poland", "Portugal",
            "Qatar",
            "Romania", "Russia", "Rwanda",
            "Saint Kitts and Nevis", "Saint Lucia", "Saint Vincent and the Grenadines", "Samoa", "San Marino", "Saudi Arabia", "Senegal", "Serbia", "Seychelles", "Sierra Leone", "Singapore", "Slovakia", "Slovenia", "Solomon Islands", "Somalia", "South Africa", "South Korea", "South Sudan", "Spain", "Sri Lanka", "Sudan", "Suriname", "Sweden", "Switzerland", "Syria",
            "Taiwan", "Tajikistan", "Tanzania", "Thailand", "Timor-Leste", "Togo", "Tonga", "Trinidad and Tobago", "Tunisia", "Turkey", "Turkmenistan", "Tuvalu",
            "Uganda", "Ukraine", "United Arab Emirates", "United Kingdom", "United States", "Uruguay", "Uzbekistan",
            "Vanuatu", "Vatican City", "Venezuela", "Vietnam",
            "Yemen",
            "Zambia", "Zimbabwe"];

        const popularCountries = ["India", "United States", "United Kingdom", "China", "Germany"];
        const listEl = document.getElementById("countryList");
        const searchBox = document.getElementById("searchBox");

        const fuse = new Fuse(countries, { includeScore: true, threshold: 0.3 });

        function showCountries(filterFn) {
            const list = filterFn ? countries.filter(filterFn) : countries;
            render(list);
        }

        function render(arr) {
            const ranked = arr.sort((a, b) => popularCountries.includes(b) - popularCountries.includes(a));
            listEl.innerHTML = ranked.map(c => `<li>${c}</li>`).join('');
        }

        function setupAlphabetButtons() {
            const container = document.getElementById("letter-buttons");
            for (let i = 65; i <= 90; i++) {
                const letter = String.fromCharCode(i);
                const btn = document.createElement("button");
                btn.textContent = letter;
                btn.onclick = () => showCountries(c => c.startsWith(letter));
                container.appendChild(btn);
            }
        }

        function aiSearch(query) {
            query = query.toLowerCase();
            if (query.includes("countries with ")) {
                const letter = query.replace("countries with ", "").charAt(0).toUpperCase();
                showCountries(c => c.startsWith(letter));
            } else {
                const results = fuse.search(query).map(result => result.item);
                render(results);
            }
        }

        searchBox.addEventListener("input", (e) => {
            aiSearch(e.target.value);
        });

        function voiceSearch() {
            const recognition = new (window.SpeechRecognition || window.webkitSpeechRecognition)();
            recognition.onresult = (event) => {
                searchBox.value = event.results[0][0].transcript;
                aiSearch(searchBox.value);
            };
            recognition.start();
        }

        setupAlphabetButtons();
        render(countries); // default all
    </script>
</body>

</html>

* {
    padding: 0;
    box-sizing: border-box;
}

body {
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    color: #fff;
    background-image: url('https://th.bing.com/th/id/OIP.Dg_aaKBaM-e9Pifhr9NVyQHaFj?rs=1&pid=ImgDetMain');
    background-size: cover;
    background-attachment: fixed;
    background-position: center;
    min-height: 100vh;
    display: flex;
    flex-direction: column;
    align-items: center;
    padding-bottom: 50px;
}

h1,
h2 {
    text-align: center;
    margin: 20px 10px;
    text-shadow: 1px 1px 2px #000;
}

.top-navbar {
    background-color: #b9bdd8;
    width: 100%;
    padding: 5px;
    /* display: flex; */
    justify-content: center;
    flex-wrap: wrap;
    position: sticky;
    top: 0;
    z-index: 10;
}

.top-navbar a {
    font-weight: bold;
    text-decoration: none;
    transition: transform 0.2s ease;
}

.top-navbar a:hover {
    color: #28a745;
    transform: scale(1.1);
}

.form-container {
    background-color: rgba(0, 0, 0, 0.7);
    border-radius: 10px;
    padding: 30px 20px;
    margin-top: 20px;
    width: 90%;
    max-width: 500px;
    box-shadow: 0 0 15px rgba(0, 0, 0, 0.4);
    display: flex;
    flex-direction: column;
    gap: 15px;
}

fieldset {
    border: none;
}

legend {
    font-size: 20px;
    font-weight: bold;
    margin-bottom: 10px;
}

.form-group {
    display: flex;
    flex-direction: column;
    gap: 5px;
}

label {
    font-weight: bold;
    font-size: 14px;
}

input,
select {
    padding: 10px;
    font-size: 14px;
    border: none;
    border-radius: 5px;
    outline: none;
    cursor: pointer;
}

input[type="submit"],
button {
    background-color: #2E7D32;
    display: inline-flex;
    align-items: center;
    justify-content: center;
    color: white;
    font-weight: 600;
    line-height: normal;
    font-size: 11px;
    padding: 3px 9px;
    border: 0px;
    margin-left: 15px;
    margin-top: 12px;
    line-height: normal;
    /* font-size: 16px; */
    width: 16%;
    border-radius: 30px;
    cursor: pointer;
    transition: background-color 0.3s ease;
}

button:hover,
input[type="submit"]:hover {
    background-color: #3c7202;
    align-items: left;
}

.trip-type {
    display: flex;
    flex-wrap: wrap;
    gap: 10px;
    margin-top: 10px;
    margin-bottom: 30px;
}

.trip-type label {
    display: flex;
    align-items: center;
    gap: 5px;
    font-weight: bold;
    color: #ddd;
}

.card {
    background-color: #fff;
    color: #000;
    padding: 15px;
    border-radius: 8px;
    box-shadow: 0 0 10px rgba(0, 0, 0, 0.3);
    margin-bottom: 15px;
    transition: transform 0.2s ease;
}

.card:hover {
    transform: scale(1.03);
}

#results-section {
    width: 90%;
    max-width: 600px;
    background-color: rgba(255, 255, 255, 0.9);
    padding: 30px;
    border-radius: 10px;
    margin-top: 20px;
    color: #000;
}

#results-section h3 {
    text-align: center;
    color: #004080;
    margin-bottom: 20px;
}

.footer {
    width: 100%;
    background-color: rgb(255 179 0 / 48%);
    color: #222;
    padding: 20px;
    text-align: left;
    margin-top: auto;
}

.footer h3 {
    font-size: 18px;
    margin-bottom: 10px;
}

.footer ul li {
    margin-bottom: 5px;
    font-size: 14px;
}

.swap-button {
    text-align: center;

    width: 40px;
    height: 40px;
    background-color: white;
    border-radius: 12px;
    display: flex;
    align-items: center;
    justify-content: center;
    /* display: inline; */
    margin-left: 30px;
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
    cursor: pointer;
    transition: box-shadow 0.3s ease;
}

.swap-button:hover {
    box-shadow: 0 6px 12px rgba(0, 0, 0, 0.15);
}

.swap-button i {
    color: #1a73e8;
    /* Google-like blue */
    font-size: 16px;
}

.margin {
    /* margin-left: 190px; */
    background-color: white;
    /* z-index: 8; */
    margin: auto;
    width: 50px;
    margin-top: -15px;
}

/* Responsive */
@media (max-width: 768px) {
    .top-navbar {
        flex-direction: column;
        gap: 10px;
        align-items: center;
    }

    .form-container {
        width: 95%;
    }

    #results-section {
        width: 95%;
    }

    .trip-type {
        flex-direction: column;
        align-items: flex-start;

    }
}

@media (max-width: 480px) {
    h1 {
        font-size: 22px;
    }

    h2 {
        font-size: 18px;
    }

    input,
    select,
    button {
        font-size: 14px;
    }

    .top-navbar {
        font-size: 14px;
    }
}

.navbar {
    display: flex;
    justify-content: space-between;
    /* Ensures separation between menu and button */
    align-items: center;
    padding: 10px 20px;
    /* background-color: #f8f8f8; */
}

.menu {
    display: flex;
    gap: 15px;
    /* Adds spacing between menu items */
}

.menu a {
    text-decoration: none;
    color: black;
    font-weight: bold;
}

.routes-grid {
    display: flex;
    flex-wrap: wrap;
    gap: 20px;
    justify-content: space-around;
    margin-top: 20px;
}

.route-box {
    background-color: #e8e4bca8;
    padding: 15px;
    border-radius: 10px;
    min-width: 220px;
    max-width: 250px;
    flex: 1 1 220px;
    box-shadow: 0 2px 8px rgba(0, 0, 0, 0.15);
    color: #000;
}

.route-box a {
    text-decoration: none;
    font-weight: 500;
}

.route-box a:hover {
    text-decoration: underline;
}

.route-box a:visited {
    color: #e81a70;
}

.faq-container {
    max-width: 800px;
    margin: 20px auto;
    padding: 1rem;
    font-family: Arial, sans-serif;
}

.faq-item {
    border: 1px solid #ddd;
    border-radius: 8px;
    margin-bottom: 10px;
    overflow: hidden;
}

.faq-question {
    padding: 15px;
    background-color: #f95757;
    cursor: pointer;
    font-weight: bold;
    transition: background-color 0.3s;
}

.faq-question .toggle {
    font-size: 1.2rem;
    color: #007bff;
    margin-left: 10px;
}

.faq-question:hover {
    background-color: #8a7a7a;
}

.faq-answer {
    padding: 15px;
    display: none;
    /* Hidden by default */
    background-color: #964949;
    border-top: 1px solid #ddd;
}

/* Hide nav links by default on small screens */
.top-navbar a {
    display: inline-block;
    padding: 0.5rem 1rem;
    text-decoration: none;
    color: #333;
}

/* Hamburger lines */
.burger {
    display: none;
    flex-direction: column;
    cursor: pointer;
}

.burger .line {
    width: 25px;
    height: 3px;
    background-color: #333;
    margin: 4px 0;
}

/* Responsive behavior */
@media (max-width: 768px) {
    .burger {
        display: flex;
    }

    .top-navbar {
        flex-direction: column;
        max-height: 60px;
        /* Initially collapsed */
        overflow: hidden;
    }

    .top-navbar.show {
        max-height: 500px;
        /* Show all items */
    }

    .top-navbar a {
        display: block;
        width: 100%;
        text-align: left;
    }
}

.burger {
    position: absolute;
    cursor: pointer;
    right: 5%;
    top: 15px;
}

.line {
    width: 33px;
    background-color: white;
    height: 4px;
    margin: 3px 3px;
}

.footer {
    /* Light background */
    padding: 20px;
}

.footer-box {
    background-color: #4677a8;
    /* Light background for footer box */
    border: 1px solid #ddd;
    /* Adds a border around the footer box */
    padding: 20px;
    max-width: 1200px;
    /* Optional: Sets the width limit for the box */
    margin: 20px auto;
    /* Centers the footer box */
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
    /* Gives a subtle shadow effect */
}

.footer-container {
    display: flex;
    flex-wrap: wrap;
    /* Makes it responsive */
    justify-content: space-between;
    /* Even spacing between columns */
}

.footer-column {
    width: 22%;
    /* Adjust the column width */
    margin-bottom: 20px;
    /* Adds spacing between rows */
}

.footer-column h3 {
    font-size: 16px;
    margin-bottom: 10px;
}

.footer-column ul {
    list-style: none;
    padding: 0;
}

.footer-column ul li {
    margin-bottom: 8px;
}

.footer-column ul li a {
    text-decoration: none;
    color: #000;
    /* Link color */
    font-size: 14px;
}

.footer-column ul li a:hover {
    text-decoration: underline;
    /* Adds hover effect */
    color: #007bff;
    /* Change color on hover */
}

@media (max-width: 768px) {
    .footer-column {
        width: 48%;
        /* Make it fit two columns on smaller screens */
    }
}

@media (max-width: 480px) {
    .footer-column {
        width: 100%;
        /* Full width for mobile */
    }
}

@media (max-width: 768px) {
    .footer-column {
        width: 48%;
        /* Make it fit two columns on smaller screens */
    }
}

@media (max-width: 480px) {
    .footer-column {
        width: 100%;
        /* Full width for mobile */
    }
}

.last {
    display: flex;
    /* Arranges items in a row */
    justify-content: center;
    /* Centers the items horizontally */
    align-items: center;
    /* Aligns items vertically */
    gap: 4rem;
    /* Adds spacing between the items */
}

.last h4 {
    margin: 0;
    /* Removes default margin for the headings */
}

.logo-container {
    display: flex;
    align-items: center;
    gap: 20px;
    padding: 10px;
}

.logo-container img {
    height: 40px;
    cursor: pointer;
}


footer {
    background-color: #865353;
    color: #333;
    padding: 48px 20px;
    font-family: Arial, sans-serif;
}

.last h4 {
    margin-bottom: 10px;
    color: #222;
}

.social-icons,
.store-icons,
.payment-icons,
.logo-container {
    display: flex;
    gap: 15px;
    align-items: center;
    flex-wrap: wrap;
    margin: 10px 0;
}

.footer-sprite {
    display: inline-block;
    width: 32px;
    height: 32px;
    background-color: #ccc;
    /* Placeholder, use icons in your actual CSS */
    border-radius: 50%;
}

.store-icons img,
.logo-container img {
    height: 40px;
    transition: transform 0.3s ease;
}

.footer-sprite,
.logo-container img {
    cursor: pointer;
}

.enlarged {
    transform: scale(1.3);
}

hr {
    border: none;
    border-top: 1px solid #ccc;
    margin: 30px 0;
}

.logo-container {
    justify-content: center;
}

.footer-copyright {
    text-align: center;
    margin-top: 20px;
    font-size: 14px;
    color: #988181;
}

.faq-container {
    max-width: 800px;
    margin: 20px auto;
}

.faq-item {
    background: #fff;
    border-radius: 8px;
    margin: 10px 0;
    box-shadow: 0 2px 8px rgba(0, 0, 0, 0.1);
    overflow: hidden;
}

.faq-question {
    font-weight: bold;
    cursor: pointer;
    padding: 16px 20px;
    position: relative;
    display: flex;
    justify-content: space-between;
    align-items: center;
}

.faq-question .arrow {
    transition: transform 0.3s ease;
}

.faq-question.active .arrow {
    transform: rotate(180deg);
}

.faq-answer {
    display: none;
    padding: 0 20px 16px;
    color: #333;
    transition: all 0.3s ease;
    line-height: 1.6;
}

.faq-answer a {
    color: #007bff;
    text-decoration: none;
}

/* Flight Booking FAQs - Collapsible style */
.faq-container {
    max-width: 900px;
    margin: 40px auto;
    padding: 0 20px;
}

.faq-item {
    background: #fff;
    border-radius: 8px;
    margin-bottom: 20px;
    padding: 10px;
    box-shadow: 0 4px 12px rgba(0, 0, 0, 0.05);
    transition: transform 0.2s ease;
}

.faq-item:hover {
    transform: translateY(-2px);
}

.faq-question {
    font-weight: bold;
    font-size: 16px;
    color: #2c3e50;
    cursor: pointer;
    margin-bottom: 10px;
}

.faq-answer {
    font-size: 14px;
    color: #555;
    line-height: 1.6;
    display: none;
    padding-left: 10px;
}

/* Collapsible effect */
.faq-answer.open {
    display: block;
}

.faq-question::after {
    content: " ▼";
    font-size: 12px;
}

.faq-question.open::after {
    content: " ▲";
}

/* Responsive for small screens */
@media (max-width: 600px) {
    .faq-container {
        padding: 0 10px;
    }

    .faq-question {
        font-size: 15px;
    }

    .faq-answer {
        font-size: 13px;
    }
}
/* Flight Booking FAQs Section */
h3 {
    text-align: center;
    margin-top: 40px;
    color: #2c3e50;
    font-size: 26px;
}

.faq-container {
    max-width: 900px;
    margin: 40px auto;
    padding: 0 20px;
}

.faq-item {
    background: #ffffff;
    border-radius: 8px;
    margin-bottom: 15px;
    padding: 20px;
    box-shadow: 0 4px 12px rgba(0, 0, 0, 0.05);
    cursor: pointer;
    transition: transform 0.3s ease;
}

.faq-item:hover {
    transform: translateY(-2px);
}

.faq-question {
    font-weight: bold;
    font-size: 16px;
    margin-bottom: 10px;
    color: #2c3e50;
}

.faq-answer {
    font-size: 14px;
    color: #f1e9e9;
    line-height: 1.6;
}

/* Responsive Design */
@media (max-width: 600px) {
    .faq-container {
        padding: 0 10px;
    }
    .faq-question {
        font-size: 15px;
    }
    .faq-answer {
        font-size: 13px;
    }
}
.holiday-video-container {
    max-width: 900px;
    margin: 40px auto;
    padding: 20px;
    background-color: #ffffff;
    border-radius: 8px;
    box-shadow: 0 4px 12px rgba(0, 0, 0, 0.05);
    text-align: center;
}

.holiday-video-container h3 {
    font-size: 26px;
    color: #2c3e50;
    margin-bottom: 20px;
}

.holiday-video-item video {
    border: 2px solid #ccc;
    border-radius: 10px;
    max-width: 100%;
}

.holiday-video-details p {
    font-size: 16px;
    color: #555;
    margin-top: 15px;
}
/* Holiday Video Section Styling */
.holiday-video-container {
    max-width: 900px;
    margin: 40px auto;
    padding: 20px;
    background-color: #ffffff;
    border-radius: 8px;
    box-shadow: 0 4px 12px rgba(0, 0, 0, 0.05);
    text-align: center;
}

.holiday-video-container h3 {
    font-size: 26px;
    color: #2c3e50;
    margin-bottom: 20px;
}

.holiday-video-item iframe {
    border: 2px solid #ccc;
    border-radius: 10px;
    max-width: 100%;
    height: 450px;
}

.holiday-video-details p {
    font-size: 16px;
    color: #555;
    margin-top: 15px;
}

// Import required modules
const express = require('express');
const mongoose = require('mongoose');
const bcrypt = require('bcryptjs');
const jwt = require('jsonwebtoken');
const stripe = require('stripe')('your_stripe_secret_key');  // Add your Stripe secret key

const app = express();
const PORT = 5000;

// Middleware
app.use(express.json());

// MongoDB connection
mongoose.connect('mongodb://localhost/goibibo', {
    useNewUrlParser: true,
    useUnifiedTopology: true
}).then(() => console.log('MongoDB Connected'))
    .catch(err => console.log(err));

// MongoDB Models
const Flight = mongoose.model('Flight', new mongoose.Schema({
    flightNumber: String,
    airline: String,
    fromCity: String,
    toCity: String,
    departureTime: String,
    arrivalTime: String,
    availableSeats: Number,
    price: Number
}));

const User = mongoose.model('User', new mongoose.Schema({
    username: { type: String, unique: true },
    email: { type: String, unique: true },
    password: String,
}));

const Booking = mongoose.model('Booking', new mongoose.Schema({
    userId: mongoose.Schema.Types.ObjectId,
    flightId: mongoose.Schema.Types.ObjectId,
    seatsBooked: Number,
    totalPrice: Number,
    paymentStatus: { type: String, default: 'Pending' }
}));

// Routes

// Register User
app.post('/users/register', async (req, res) => {
    const { username, email, password } = req.body;
    try {
        const salt = await bcrypt.genSalt(10);
        const hashedPassword = await bcrypt.hash(password, salt);
        const newUser = new User({ username, email, password: hashedPassword });
        await newUser.save();
        res.status(201).json({ message: 'User registered successfully' });
    } catch (err) {
        res.status(400).json({ error: err.message });
    }
});

// Login User
app.post('/users/login', async (req, res) => {
    const { username, password } = req.body;
    const user = await User.findOne({ username });

    if (!user) {
        return res.status(400).json({ message: 'User not found' });
    }

    const isMatch = await bcrypt.compare(password, user.password);

    if (!isMatch) {
        return res.status(400).json({ message: 'Invalid credentials' });
    }

    const token = jwt.sign({ userId: user._id }, 'secret_key', { expiresIn: '1h' });
    res.status(200).json({ message: 'Login successful', token });
});

// Search Flights
app.get('/flights', async (req, res) => {
    const { from, to, date } = req.query;
    const flights = await Flight.find({ fromCity: from, toCity: to, departureTime: { $gte: date } });
    res.status(200).json(flights);
});

// Book Flight
app.post('/bookings', async (req, res) => {
    const { userId, flightId, seatsBooked, totalPrice } = req.body;

    // Create booking
    const booking = new Booking({
        userId,
        flightId,
        seatsBooked,
        totalPrice
    });

    await booking.save();

    // Update flight available seats
    const flight = await Flight.findById(flightId);
    flight.availableSeats -= seatsBooked;
    await flight.save();

    res.status(200).json(booking);
});

// Payment (Stripe)
app.post('/payment', async (req, res) => {
    const { amount } = req.body;

    try {
        const paymentIntent = await stripe.paymentIntents.create({
            amount: amount * 100,  // Amount is in cents
            currency: 'usd',
        });

        res.status(200).json({ clientSecret: paymentIntent.client_secret });
    } catch (err) {
        res.status(500).json({ error: err.message });
    }
});

// Start the server
app.listen(PORT, () => {
    console.log(`Server is running on port ${PORT}`);
});
/* General Styles */
body {
    font-family: Arial, sans-serif;
    margin: 0;
    padding: 0;
    background-image: url('https://c4.wallpaperflare.com/wallpaper/123/702/385/technology-bitcoin-coin-cryptocurrency-money-hd-wallpaper-preview.jpg');
    color: #333;
  }
  
  /* Forex Section */
  .forex-section {
    max-width: 600px;
    margin: 2rem auto;
    padding: 1.5rem;
    background-color: #ffffff;
    border-radius: 10px;
    box-shadow: 0px 4px 6px rgba(0, 0, 0, 0.1);
  }
  
  .forex-box h3 {
    margin-bottom: 1rem;
    text-align: center;
    color: #444;
    font-size: 1.8rem;
  }
  
  /* Fields */
  .fields {
    display: flex;
    flex-direction: column;
    gap: 1rem;
  }
  
  .field label {
    font-weight: bold;
    margin-bottom: 0.5rem;
    display: block;
  }
  
  .field select,
  .field input {
    width: 100%;
    padding: 0.8rem;
    border: 1px solid #ccc;
    border-radius: 5px;
  }
  
  .field input:focus,
  .field select:focus {
    outline: none;
    border: 1px solid #007bff;
    box-shadow: 0px 0px 5px rgba(0, 123, 255, 0.5);
  }
  
  /* Convert Button */
  .field button {
    width: 100%;
    padding: 0.8rem;
    background-color: #007bff;
    color: white;
    border: none;
    border-radius: 5px;
    font-size: 1rem;
    font-weight: bold;
    cursor: pointer;
  }
  
  .field button:hover {
    background-color: #0056b3;
  }
  
  /* Result Section */
  .result {
    margin-top: 1.5rem;
    text-align: center;
  }
  
  .result h4 {
    font-size: 1.2rem;
    margin-bottom: 0.5rem;
  }
  
  .result p {
    font-size: 1rem;
    color: #444;
  }
  

  button#convertBtn {
    padding: 12px 20px;
    background-color: #007bff;
    color: #244824;
    border: none;
    border-radius: 8px;
    font-size: 16px;
    cursor: pointer;
    transition: background 0.3s;
}

button#convertBtn:hover {
    background-color: #0056b3;
}
.card {
  background-color: #fff;
  border-radius: 15px;
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
  padding: 20px;
  max-width: 300px;
  margin: 20px auto;
  transition: transform 0.3s ease-in-out;
}

.card h2 {
  font-size: 1.8em;
  color: #333;
  margin-bottom: 10px;
  text-align: center;
  font-family: 'Arial', sans-serif;
}

.card h3 {
  font-size: 1.2em;
  color: #555;
  margin: 10px 0;
  text-align: center;
  font-family: 'Arial', sans-serif;
  transition: color 0.3s ease;
}

.card h3:hover {
  color: #007BFF;
  cursor: pointer;
}

.card:hover {
  transform: translateY(-10px);
}

.card::before {
  content: '';
  display: block;
  position: absolute;
  top: 0;
  left: 50%;
  width: 80%;
  height: 5px;
  background-color: #007BFF;
  border-radius: 5px;
  transform: translateX(-50%);
}
.footer {
  background-color: #000;
  color: #fff;
  padding: 20px;
  text-align: left;
}

.footer-logo-section {
  margin-bottom: 20px;
}

.footer-logo {
  width: 120px; /* Adjust size */
}

.footer-links-section h3,
.footer-social-section h3 {
  font-size: 1.2em;
}

.footer-links-section ul,
.footer-social-section ul {
  list-style-type: none;
  padding: 0;
}

.footer-links-section li,
.footer-social-section li {
  margin: 5px 0;
}

.footer-links-section a,
.footer-social-section a {
  color: #fff;
  text-decoration: none;
  transition: color 0.3s;
}

.footer-links-section a:hover,
.footer-social-section a:hover {
  color: #007BFF; /* Highlight color */
}


.social-icons a {
  display: inline-block;
  color: #ccc;
  margin: 0 10px;
  font-size: 20px;
  transition: color 0.3s;
}

.social-icons a:hover {
  color: #ffffff;
}

.store-icons {
  margin: 15px 0;
}

.store-icons a {
  display: inline-block;
  margin: 10px;
}
.social-icons img {
  width: 24px;
  height: 24px;
  display: inline-block;
}

.footer-copyright {
  font-size: 0.9em;
  text-align: right;
  margin-top: 20px;
}
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Forex Exchange</title>
    <!-- <link rel="stylesheet" href="Forex.css" /> -->
    <link rel="stylesheet" href="styleAir.css">
</head>
<style>
    /* General Styles */
    body {
        font-family: Arial, sans-serif;
        margin: 0;
        padding: 0;
        background-image: url('https://c4.wallpaperflare.com/wallpaper/123/702/385/technology-bitcoin-coin-cryptocurrency-money-hd-wallpaper-preview.jpg');
        color: #333;
    }

    /* Forex Section */
    .forex-section {
        max-width: 600px;
        margin: 2rem auto;
        padding: 1.5rem;
        background-color: #ffffff;
        border-radius: 10px;
        box-shadow: 0px 4px 6px rgba(0, 0, 0, 0.1);
    }

    .forex-box h3 {
        margin-bottom: 1rem;
        text-align: center;
        color: #444;
        font-size: 1.8rem;
    }

    /* Fields */
    .fields {
        display: flex;
        flex-direction: column;
        gap: 1rem;
    }

    .field label {
        font-weight: bold;
        margin-bottom: 0.5rem;
        display: block;
    }

    .field select,
    .field input {
        width: 100%;
        padding: 0.8rem;
        border: 1px solid #ccc;
        border-radius: 5px;
    }

    .field input:focus,
    .field select:focus {
        outline: none;
        border: 1px solid #007bff;
        box-shadow: 0px 0px 5px rgba(0, 123, 255, 0.5);
    }

    /* Convert Button */
    .field button {
        width: 100%;
        padding: 0.8rem;
        background-color: #007bff;
        color: white;
        border: none;
        border-radius: 5px;
        font-size: 1rem;
        font-weight: bold;
        cursor: pointer;
    }

    .field button:hover {
        background-color: #0056b3;
    }

    /* Result Section */
    .result {
        margin-top: 1.5rem;
        text-align: center;
    }

    .result h4 {
        font-size: 1.2rem;
        margin-bottom: 0.5rem;
    }

    .result p {
        font-size: 1rem;
        color: #444;
    }


    button#convertBtn {
        padding: 12px 20px;
        background-color: #007bff;
        color: #244824;
        border: none;
        border-radius: 8px;
        font-size: 16px;
        cursor: pointer;
        transition: background 0.3s;
    }

    button#convertBtn:hover {
        background-color: #0056b3;
    }

    .card {
        background-color: #fff;
        border-radius: 15px;
        box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
        padding: 20px;
        max-width: 300px;
        margin: 20px auto;
        transition: transform 0.3s ease-in-out;
    }

    .card h2 {
        font-size: 1.8em;
        color: #333;
        margin-bottom: 10px;
        text-align: center;
        font-family: 'Arial', sans-serif;
    }

    .card h3 {
        font-size: 1.2em;
        color: #555;
        margin: 10px 0;
        text-align: center;
        font-family: 'Arial', sans-serif;
        transition: color 0.3s ease;
    }

    .card h3:hover {
        color: #007BFF;
        cursor: pointer;
    }

    .card:hover {
        transform: translateY(-10px);
    }

    .card::before {
        content: '';
        display: block;
        position: absolute;
        top: 0;
        left: 50%;
        width: 80%;
        height: 5px;
        background-color: #007BFF;
        border-radius: 5px;
        transform: translateX(-50%);
    }

    .footer {
        background-color: #000;
        color: #fff;
        padding: 20px;
        text-align: left;
    }

    .footer-logo-section {
        margin-bottom: 20px;
    }

    .footer-logo {
        width: 120px;
        /* Adjust size */
    }

    .footer-links-section h3,
    .footer-social-section h3 {
        font-size: 1.2em;
    }

    .footer-links-section ul,
    .footer-social-section ul {
        list-style-type: none;
        padding: 0;
    }

    .footer-links-section li,
    .footer-social-section li {
        margin: 5px 0;
    }

    .footer-links-section a,
    .footer-social-section a {
        color: #fff;
        text-decoration: none;
        transition: color 0.3s;
    }

    .footer-links-section a:hover,
    .footer-social-section a:hover {
        color: #007BFF;
        /* Highlight color */
    }


    .social-icons a {
        display: inline-block;
        color: #ccc;
        margin: 0 10px;
        font-size: 20px;
        transition: color 0.3s;
    }

    .social-icons a:hover {
        color: #ffffff;
    }

    .store-icons {
        margin: 15px 0;
    }

    .store-icons a {
        display: inline-block;
        margin: 10px;
    }

    .social-icons img {
        width: 24px;
        height: 24px;
        display: inline-block;
    }

    .footer-copyright {
        font-size: 0.9em;
        text-align: right;
        margin-top: 20px;
    }
</style>

<body>
    <div class="forex-section">
        <div class="forex-box">
            <h3>💱 Forex Exchange</h3>
            <div class="fields">
                <div class="field">
                    <label>Base Currency</label>
                    <select>
                        <option value="INR">Indian Currency (INR)</option>
                        <option value="AUD">Australian Dollar (AUD)</option>
                        <option value="CAD">Canadian Dollar (CAD)</option>
                        <option value="JPY">Japanese Yen (JPY)</option>
                        <option value="CNY">Chinese Yuan (CNY)</option>
                        <option value="MXN">Mexican Peso (MXN)</option>
                        <option value="BRL">Brazilian Real (BRL)</option>
                        <option value="SAR">Saudi Riyal (SAR)</option>
                        <option value="ZAR">South African Rand (ZAR)</option>
                        <option value="RUB">Russian Ruble (RUB)</option>
                        <option value="CHF">Swiss Franc (CHF)</option>
                        <option value="HKD">Hong Kong Dollar (HKD)</option>
                        <option value="SGD">Singapore Dollar (SGD)</option>
                        <option value="NZD">New Zealand Dollar (NZD)</option>
                        <option value="KRW">South Korean Won (KRW)</option>
                        <option value="TRY">Turkish Lira (TRY)</option>
                        <option value="AED">United Arab Emirates Dirham (AED)</option>
                        <option value="MYR">Malaysian Ringgit (MYR)</option>
                        <option value="THB">Thai Baht (THB)</option>
                        <option value="IDR">Indonesian Rupiah (IDR)</option>
                        <option value="SEK">Swedish Krona (SEK)</option>
                    </select>
                </div>
                <div class="field">
                    <label>Target Currency</label>
                    <select>
                        <option value="INR">Indian Currency (INR)</option>
                        <option value="AUD">Australian Dollar (AUD)</option>
                        <option value="CAD">Canadian Dollar (CAD)</option>
                        <option value="JPY">Japanese Yen (JPY)</option>
                        <option value="CNY">Chinese Yuan (CNY)</option>
                        <option value="MXN">Mexican Peso (MXN)</option>
                        <option value="BRL">Brazilian Real (BRL)</option>
                        <option value="SAR">Saudi Riyal (SAR)</option>
                        <option value="ZAR">South African Rand (ZAR)</option>
                        <option value="RUB">Russian Ruble (RUB)</option>
                        <option value="CHF">Swiss Franc (CHF)</option>
                        <option value="HKD">Hong Kong Dollar (HKD)</option>
                        <option value="SGD">Singapore Dollar (SGD)</option>
                        <option value="NZD">New Zealand Dollar (NZD)</option>
                        <option value="KRW">South Korean Won (KRW)</option>
                        <option value="TRY">Turkish Lira (TRY)</option>
                        <option value="AED">United Arab Emirates Dirham (AED)</option>
                        <option value="MYR">Malaysian Ringgit (MYR)</option>
                        <option value="THB">Thai Baht (THB)</option>
                        <option value="IDR">Indonesian Rupiah (IDR)</option>
                        <option value="SEK">Swedish Krona (SEK)</option>
                        <!-- Add more currencies as needed -->
                    </select>
                </div>
                <div class="field">
                    <label>Amount</label>
                    <input type="number" placeholder="Enter amount" />
                </div>
            </div>
            <div class="result">
                <h4>Conversion Result:</h4>
                <p id="conversionResult">--</p>
                <button type="submit" id="convertBtn">Convert</button>
            </div>
        </div>
    </div>
    <script src="Forex.js" defer></script>
    <footer class="footer">
        <div class="footer-links-section">
            <h3>QUICK LINKS</h3>
            <ul>
                <li><a href="privacy-policy.html">Privacy Policy</a></li>
                <li><a href="terms.html">Terms of Service</a></li>
            </ul>
        </div>
        <div class="footer-social-section">
            <h3>FOLLOW US</h3>
            <!-- Facebook -->
            <div class="social-icons">
                <a href="https://www.facebook.com" target="_blank"><img
                        src="https://tripmoneycmsimgak.mmtcdn.com/img/fb_Icon_8eab71f726.png" loading="lazy"
                        alt="Fb icon" class="" id="" width="29" height="26">
                    <!-- Twitter -->
                    <a id="listingPage_footer_twitterLink" aria-label="twitter"
                        href="https://mobile.twitter.com/tripmoneymmt" target="_blank" rel="noopener noreferrer">
                        <div class="LandingFooterstyle__IconMargin-sc-1ahd1n-2 cNlxoh">
                            <picture>
                                <source
                                    srcset="https://tripmoneycmsimgak.mmtcdn.com/img/twitter_Icon_760f145ad2.png?im=Resize=(29) 29w, https://tripmoneycmsimgak.mmtcdn.com/img/twitter_Icon_760f145ad2.png?im=Resize=(58) 58w, https://tripmoneycmsimgak.mmtcdn.com/img/twitter_Icon_760f145ad2.png?im=Resize=(87) 87w"
                                    sizes="(max-width: 29px) 29px, (max-width: 58px) 58px, 87px">
                                <img src="https://tripmoneycmsimgak.mmtcdn.com/img/twitter_Icon_760f145ad2.png"
                                    loading="lazy" alt="Twitter Icon" width="29" height="26">
                            </picture>
                        </div>
                    </a>

                    <!-- Linkedin -->
                    <a id="listingPage_footer_linkedInLink" aria-label="linkedin"
                        href="https://www.linkedin.com/company/trip-money" target="_blank" rel="noopener noreferrer">
                        <div class="LandingFooterstyle__IconMargin-sc-1ahd1n-2 cNlxoh">
                            <picture>
                                <source data-testid="testID"
                                    srcset="https://tripmoneycmsimgak.mmtcdn.com/img/Linkedin_Icon_fec59ba5c7.png?im=Resize=(29) 29w,https://tripmoneycmsimgak.mmtcdn.com/img/Linkedin_Icon_fec59ba5c7.png?im=Resize=(58) 58w,https://tripmoneycmsimgak.mmtcdn.com/img/Linkedin_Icon_fec59ba5c7.png?im=Resize=(87) 87w"
                                    sizes="29"><img
                                    src="https://tripmoneycmsimgak.mmtcdn.com/img/Linkedin_Icon_fec59ba5c7.png"
                                    loading="lazy" alt="Linkedin Icon" class="" id="" width="29" height="26">
                            </picture>
                        </div>
                    </a>
            </div>
        </div>

        <div class="footer-copyright">
            <p>© 2025 MakeMyTrip (India) Private Limited | Country India</p>
        </div>
    </footer>

</body>

</html>
document.addEventListener("DOMContentLoaded", function () {
    const convertBtn = document.getElementById("convertBtn");
    const resultDisplay = document.getElementById("conversionResult");

    convertBtn.addEventListener("click", async function () {
        const selects = document.querySelectorAll("select");
        const baseCurrency = selects[0].value;
        const targetCurrency = selects[1].value;
        const amount = parseFloat(document.querySelector("input[type='number']").value);

        if (isNaN(amount) || amount <= 0) {
            resultDisplay.textContent = "Please enter a valid amount.";
            return;
        }

        try {
            const response = await fetch(`https://api.exchangerate-api.com/v4/latest/${baseCurrency}`);
            const data = await response.json();
            const rate = data.rates[targetCurrency];

            if (!rate) {
                resultDisplay.textContent = "Conversion rate not available.";
                return;
            }

            const convertedAmount = (amount * rate).toFixed(2);
            resultDisplay.textContent = `${amount} ${baseCurrency} = ${convertedAmount} ${targetCurrency}`;
        } catch (error) {
            console.error(error);
            resultDisplay.textContent = "Failed to fetch exchange rate.";
        }
    });
});
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Flight Status Updates</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <div class="flight-status-container">
        <div class="flight-status" id="flightStatus">
            <div class="status">Flight AA123 - On Time</div>
            <div class="status">Flight BA456 - Delayed</div>
            <div class="status">Flight CA789 - Cancelled</div>
        </div>
    </div>
    <script src="script.js"></script>
</body>
</html>
<!DOCTYPE html>
<html lang="en">

<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Goibibo Style Popup</title>
  <style>
    body {
      margin: 0;
      font-family: Arial, sans-serif;
      background-color: #f0f0f0;
    }

    .modal {
      display: flex;
      justify-content: center;
      align-items: center;
      position: fixed;
      z-index: 9999;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      background-color: rgba(0, 0, 0, 0.6);
    }

    .modal-box {
      background-color: white;
      width: 90%;
      max-width: 800px;
      display: flex;
      border-radius: 16px;
      overflow: hidden;
      box-shadow: 0 5px 20px rgba(0, 0, 0, 0.3);
      animation: scaleIn 0.3s ease-in-out;
      position: relative;
    }

    .promo {
      width: 50%;
      background-color: #fce4ec;
    }

    .promo img {
      width: 100%;
      height: 100%;
      object-fit: cover;
    }

    .login {
      width: 50%;
      padding: 30px;
      box-sizing: border-box;
    }

    .close-btn {
      position: absolute;
      top: 10px;
      right: 15px;
      font-size: 24px;
      font-weight: bold;
      color: #444;
      cursor: pointer;
    }

    input[type="tel"] {
      width: 100%;
      padding: 10px;
      font-size: 16px;
      margin-top: 10px;
      border: 1px solid #ccc;
      border-radius: 6px;
    }

    .btn {
      margin-top: 20px;
      width: 100%;
      padding: 12px;
      font-size: 16px;
      border: none;
      background-color: #ccc;
      color: #fff;
      border-radius: 6px;
      cursor: not-allowed;
    }

    h2 {
      margin-bottom: 10px;
    }

    @keyframes scaleIn {
      from {
        opacity: 0;
        transform: scale(0.95);
      }

      to {
        opacity: 1;
        transform: scale(1);
      }
    }

    @media (max-width: 768px) {
      .modal-box {
        flex-direction: column;
      }

      .promo,
      .login {
        width: 100%;
      }

      .promo {
        height: 200px;
      }
    }
  </style>
</head>

<body>
  <div class="modal" id="popup">
    <div class="modal-box">
      <div class="promo">
        <img src="049b5c68-e732-4202-9f88-a06ca90e7ad3.png" alt="Promo" />
      </div>
      <div class="login">
        <span class="close-btn" onclick="closePopup()">&times;</span>
        <h2>Login/Signup</h2>
        <label>Enter your Mobile Number</label><br>
        <input type="tel" placeholder="+91" /><br>
        <button class="btn" disabled>Continue</button>
        <p style="margin-top: 20px; font-size: 12px;">
          By proceeding, you agree to our <a href="#">Privacy Policy</a>,
          <a href="#">User Agreement</a>, and <a href="#">Terms of Service</a>.
        </p>
      </div>
    </div>
  </div>

  <script>
    function closePopup() {
      document.getElementById("popup").style.display = "none";
    }

    // Show the popup on page load
    window.onload = () => {
      document.getElementById("popup").style.display = "flex";
    };
  </script>
</body>

</html>
<!DOCTYPE html>
<html lang="en">

<head>
  <meta charset="UTF-8" />
  <title>Airline Reservation System</title>
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.0/css/all.min.css" />
  <link rel="stylesheet" href="airline.css" />
  <style>
    /* Include your CSS here if you want it embedded instead of linked */
  </style>
</head>

<body>
  <div class="background"></div>
  <h1>Your Experience Starts Here!</h1>
  <h2>Airline Reservation System</h2>

  <div class="top-navbar">
    <a href="#" id="nav-flights"><i class="fas fa-plane"></i> Flights</a>
    <a href="#" id="nav-hotels"><i class="fas fa-hotel"></i> Hotels</a>
    <a href="#" id="nav-trains"><i class="fas fa-train"></i> Trains</a>
    <a href="#" id="nav-taxi"><i class="fas fa-taxi"></i> Cabs</a>
    <a href="#" id="nav-bus"><i class="fas fa-bus"></i> Bus</a>
    <a href="#" id="nav-umbrella-beach"><i class="fas fa-umbrella-beach"></i> Holidays</a>
    <a href="#" id="nav-dollar-sign"><i class="fas fa-dollar-sign"></i> Forex</a>
  </div>

  <div id="flight-section" class="form-container">
    <form id="flightForm">
      <fieldset>
        <legend>Trip Details</legend>

        <div class="trip-type">
          <label><input type="radio" name="trip" value="one-way" checked /> One-way</label>
          <label><input type="radio" name="trip" value="round-trip" /> Round-trip</label>
          <label><input type="radio" name="trip" value="multi-city" /> Multi-city</label>
        </div>

        <div class="form-content with-arrow">
          <div class="form-group">
            <label for="source">Source:</label>
            <select id="source" name="source" required>
              <option value="" disabled selected>Enter your source</option>
              <option value="India">India</option>
              <option value="UK">United Kingdom</option>
              <option value="Thailand">Thailand</option>
              <option value="Russia">Russia</option>
              <option value="Japan">Japan</option>
              <option value="Norway">Norway</option>
              <option value="Malaysia">Malaysia</option>
            </select>
          </div>

          <div class="form-group">
            <label for="destination">Destination:</label>
            <select id="destination" name="destination" required>
              <option value="" disabled selected>Enter your destination</option>
              <option value="Dubai">Dubai</option>
              <option value="Scotland">Scotland</option>
              <option value="Goa">Goa</option>
              <option value="India">India</option>
              <option value="UK">United Kingdom</option>
              <option value="Thailand">Thailand</option>
            </select>
          </div>
        </div>

        <div class="form-group">
          <label for="travellers">Travellers:</label>
          <input type="number" value="1" min="1" id="travellers" name="travellers" required />
        </div>

        <div class="form-group">
          <label for="class">Class:</label>
          <select id="class" name="class" required>
            <option value="General">General</option>
            <option value="Economy">Economy</option>
            <option value="Premium Economy">Premium Economy</option>
            <option value="Business">Business Class</option>
          </select>
        </div>

        <div class="form-group">
          <label for="offers">Offers:</label>
          <input type="text" id="offers" name="offers" placeholder="E.g., NewUser, SummerSale" />
        </div>

        <button type="submit" id="bookBtn">Book Flight</button>
        <button type="button" id="searchBtn">Search Flights</button>
      </fieldset>
    </form>

    <div class="trip-type">
      <label><input type="checkbox" name="category1" /> Student</label>
      <label><input type="checkbox" name="category2" /> Senior citizen</label>
      <label><input type="checkbox" name="category3" /> Armed forces</label>
      <label><input type="checkbox" name="category4" /> Doctors & Nurses</label>
    </div>
  </div>

  <div id="results-section" style="display: none;">
    <h3 id="results-title"></h3>
    <div id="results-container"></div>
    <button id="backBtn">← Back</button>
  </div>

  <footer class="footer">
    <h3>Popular Flight Routes</h3>
    <ul>
      <li>Delhi → Mumbai, Pune, Bangalore</li>
      <li>Goa → Mumbai, Indore, Delhi</li>
      <li>Pune → Delhi, Nagpur, Kolkata</li>
    </ul>
  </footer>

  <script>
    document.addEventListener("DOMContentLoaded", function () {
      let actionType = "book"; // default action

      const navFlights = document.getElementById("nav-flights");
      const navHotels = document.getElementById("nav-hotels");
      const navTrains = document.getElementById("nav-trains");

      const flightSection = document.getElementById("flight-section");
      const resultsSection = document.getElementById("results-section");
      const resultsTitle = document.getElementById("results-title");
      const resultsContainer = document.getElementById("results-container");
      const backBtn = document.getElementById("backBtn");

      const bookBtn = document.getElementById("bookBtn");
      const searchBtn = document.getElementById("searchBtn");
      const flightForm = document.getElementById("flightForm");

      navFlights.addEventListener("click", function (e) {
        e.preventDefault();
        flightSection.style.display = "block";
        resultsSection.style.display = "none";
      });

      navHotels.addEventListener("click", async function (e) {
        e.preventDefault();
        try {
          const res = await fetch("http://localhost:5000/api/hotels");
          const data = await res.json();
          displayResults("Hotels", data);
        } catch (error) {
          alert("Error fetching hotel data!");
        }
      });

      navTrains.addEventListener("click", async function (e) {
        e.preventDefault();
        try {
          const res = await fetch("http://localhost:5000/api/trains");
          const data = await res.json();
          displayResults("Trains", data);
        } catch (error) {
          alert("Error fetching train data!");
        }
      });

      backBtn.addEventListener("click", function () {
        resultsSection.style.display = "none";
        flightSection.style.display = "block";
      });

      function displayResults(title, data) {
        flightSection.style.display = "none";
        resultsSection.style.display = "block";
        resultsTitle.textContent = title;
        resultsContainer.innerHTML = data
          .map(
            (item) => `
              <div class="card">
                <h4>${item.name}</h4>
                <p>${item.location || item.description || "No details available"}</p>
              </div>
            `
          )
          .join("");
      }

      bookBtn.addEventListener("click", () => {
        actionType = "book";
      });

      searchBtn.addEventListener("click", () => {
        actionType = "search";
        flightForm.dispatchEvent(new Event("submit"));
      });

      flightForm.addEventListener("submit", async function (e) {
        e.preventDefault();
        const formData = new FormData(flightForm);
        const data = {};
        formData.forEach((value, key) => {
          data[key] = value;
        });

        const url = actionType === "book" ? "http://localhost:5000/book" : "http://localhost:5000/search";

        try {
          const res = await fetch(url, {
            method: "POST",
            headers: { "Content-Type": "application/json" },
            body: JSON.stringify(data),
          });

          const result = await res.json();
          alert(result.message);
        } catch (err) {
          alert("Something went wrong!");
          console.error(err);
        }
      });
    });
  </script>
</body>

</html>
/* Global Styles */
body {
    font-family: 'Segoe UI', sans-serif;
    margin: 0;
    padding: 0;
    background: #f8f9fa;
    color: #333;
}

h3 {
    text-align: center;
    margin-top: 40px;
    color: #2c3e50;
}

/* Search Section */
.search-section {
    background: linear-gradient(135deg, #2e86de, #74b9ff);
    padding: 40px 20px;
    display: flex;
    justify-content: center;
    align-items: center;
}

.search-box {
    background: white;
    border-radius: 12px;
    padding: 30px;
    max-width: 900px;
    width: 100%;
    box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
}

.tabs {
    display: flex;
    justify-content: space-around;
    margin-bottom: 20px;
}

.tab {
    padding: 10px 20px;
    cursor: pointer;
    border-radius: 20px;
    font-weight: 500;
    transition: background 0.3s ease;
}

.tab.active {
    background: #2e86de;
    color: white;
}

.fields {
    display: flex;
    flex-wrap: wrap;
    gap: 20px;
    margin-bottom: 20px;
}

.field {
    flex: 1 1 200px;
    display: flex;
    flex-direction: column;
}

.field label {
    font-size: 14px;
    margin-bottom: 6px;
    font-weight: 500;
}

.field input,
.field select {
    padding: 10px;
    border: 1px solid #ccc;
    border-radius: 6px;
    font-size: 14px;
}

.search-btn {
    text-align: center;
}

.search-btn button {
    padding: 12px 30px;
    background: #27ae60;
    color: white;
    font-weight: bold;
    font-size: 16px;
    border: none;
    border-radius: 8px;
    cursor: pointer;
    transition: background 0.3s ease;
}

.search-btn button:hover {
    background: #219150;
}

/* Card Row */
.card-row {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    gap: 30px;
    padding: 40px 20px;
}

.card {
    background: white;
    border-radius: 12px;
    overflow: hidden;
    box-shadow: 0 4px 10px rgba(0, 0, 0, 0.08);
    max-width: 300px;
    transition: transform 0.3s ease;
}

.card:hover {
    transform: translateY(-5px);
}

.card-img {
    width: 100%;
    height: 180px;
    object-fit: cover;
}

.card-content {
    padding: 20px;
}

.card-content h3 {
    margin: 0 0 10px;
    font-size: 20px;
    color: #34495e;
}

.card-content p {
    margin: 4px 0;
    font-size: 14px;
}

.price {
    color: #e74c3c;
    font-weight: bold;
    margin-top: 10px;
}

.book-btn {
    margin-top: 15px;
    padding: 10px 20px;
    background: #2e86de;
    color: white;
    border: none;
    border-radius: 6px;
    cursor: pointer;
    transition: background 0.3s ease;
}

.book-btn:hover {
    background: #1b65b0;
}

/* FAQs */
.faq-container {
    max-width: 900px;
    margin: 40px auto;
    padding: 0 20px;
}

.faq-item {
    background: white;
    border-radius: 8px;
    margin-bottom: 15px;
    padding: 20px;
    box-shadow: 0 2px 8px rgba(0, 0, 0, 0.05);
}

.faq-question {
    font-weight: bold;
    margin-bottom: 10px;
    color: #2c3e50;
}

.faq-answer {
    font-size: 14px;
    color: #555;
}

/* Responsive */
@media (max-width: 768px) {
    .fields {
        flex-direction: column;
    }

    .card-row {
        flex-direction: column;
        align-items: center;
    }

    .search-box {
        padding: 20px;
    }
}

/* Holiday Video Section */
.holiday-video-container {
    max-width: 900px;
    margin: 40px auto;
    padding: 20px;
    background-color: #ffffff;
    border-radius: 8px;
    box-shadow: 0 4px 12px rgba(0, 0, 0, 0.05);
    text-align: center;
}

.holiday-video-container h3 {
    font-size: 26px;
    color: #2c3e50;
    margin-bottom: 20px;
}

.holiday-video-item video {
    border: 2px solid #ccc;
    border-radius: 10px;
    max-width: 100%;
}

.holiday-video-details p {
    font-size: 16px;
    color: #555;
    margin-top: 15px;
}


.holiday-video-item iframe {
    border: 2px solid #ccc;
    border-radius: 10px;
    max-width: 100%;
    height: 450px;
}

.holiday-video-details p {
    font-size: 16px;
    color: #555;
    margin-top: 15px;
}
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Travel Search</title>
    <!-- <link rel="stylesheet" href="Holidays.css" /> -->
    <!-- <link rel="stylesheet" href="styleAir.css"> -->
</head>
<style>
    /* Global Styles */
    body {
        font-family: 'Segoe UI', sans-serif;
        margin: 0;
        padding: 0;
        background: #f8f9fa;
        color: #333;
    }

    h3 {
        text-align: center;
        margin-top: 40px;
        color: #2c3e50;
    }

    /* Search Section */
    .search-section {
        background: linear-gradient(135deg, #2e86de, #74b9ff);
        padding: 40px 20px;
        display: flex;
        justify-content: center;
        align-items: center;
    }

    .search-box {
        background: white;
        border-radius: 12px;
        padding: 30px;
        max-width: 900px;
        width: 100%;
        box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
    }

    .tabs {
        display: flex;
        justify-content: space-around;
        margin-bottom: 20px;
    }

    .tab {
        padding: 10px 20px;
        cursor: pointer;
        border-radius: 20px;
        font-weight: 500;
        transition: background 0.3s ease;
    }

    .tab.active {
        background: #2e86de;
        color: white;
    }

    .fields {
        display: flex;
        flex-wrap: wrap;
        gap: 20px;
        margin-bottom: 20px;
    }

    .field {
        flex: 1 1 200px;
        display: flex;
        flex-direction: column;
    }

    .field label {
        font-size: 14px;
        margin-bottom: 6px;
        font-weight: 500;
    }

    .field input,
    .field select {
        padding: 10px;
        border: 1px solid #ccc;
        border-radius: 6px;
        font-size: 14px;
    }

    .search-btn {
        text-align: center;
    }

    .search-btn button {
        padding: 12px 30px;
        background: #27ae60;
        color: white;
        font-weight: bold;
        font-size: 16px;
        border: none;
        border-radius: 8px;
        cursor: pointer;
        transition: background 0.3s ease;
    }

    .search-btn button:hover {
        background: #219150;
    }

    /* Card Row */
    .card-row {
        display: flex;
        flex-wrap: wrap;
        justify-content: center;
        gap: 30px;
        padding: 40px 20px;
    }

    .card {
        background: white;
        border-radius: 12px;
        overflow: hidden;
        box-shadow: 0 4px 10px rgba(0, 0, 0, 0.08);
        max-width: 300px;
        transition: transform 0.3s ease;
    }

    .card:hover {
        transform: translateY(-5px);
    }

    .card-img {
        width: 100%;
        height: 180px;
        object-fit: cover;
    }

    .card-content {
        padding: 20px;
    }

    .card-content h3 {
        margin: 0 0 10px;
        font-size: 20px;
        color: #34495e;
    }

    .card-content p {
        margin: 4px 0;
        font-size: 14px;
    }

    .price {
        color: #e74c3c;
        font-weight: bold;
        margin-top: 10px;
    }

    .book-btn {
        margin-top: 15px;
        padding: 10px 20px;
        background: #2e86de;
        color: white;
        border: none;
        border-radius: 6px;
        cursor: pointer;
        transition: background 0.3s ease;
    }

    .book-btn:hover {
        background: #1b65b0;
    }

    /* FAQs */
    .faq-container {
        max-width: 900px;
        margin: 40px auto;
        padding: 0 20px;
    }

    .faq-item {
        background: white;
        border-radius: 8px;
        margin-bottom: 15px;
        padding: 20px;
        box-shadow: 0 2px 8px rgba(0, 0, 0, 0.05);
    }

    .faq-question {
        font-weight: bold;
        margin-bottom: 10px;
        color: #2c3e50;
    }

    .faq-answer {
        font-size: 14px;
        color: #555;
    }

    /* Responsive */
    @media (max-width: 768px) {
        .fields {
            flex-direction: column;
        }

        .card-row {
            flex-direction: column;
            align-items: center;
        }

        .search-box {
            padding: 20px;
        }
    }

    /* Holiday Video Section */
    .holiday-video-container {
        max-width: 900px;
        margin: 40px auto;
        padding: 20px;
        background-color: #ffffff;
        border-radius: 8px;
        box-shadow: 0 4px 12px rgba(0, 0, 0, 0.05);
        text-align: center;
    }

    .holiday-video-container h3 {
        font-size: 26px;
        color: #2c3e50;
        margin-bottom: 20px;
    }

    .holiday-video-item video {
        border: 2px solid #ccc;
        border-radius: 10px;
        max-width: 100%;
    }

    .holiday-video-details p {
        font-size: 16px;
        color: #555;
        margin-top: 15px;
    }


    .holiday-video-item iframe {
        border: 2px solid #ccc;
        border-radius: 10px;
        max-width: 100%;
        height: 450px;
    }

    .holiday-video-details p {
        font-size: 16px;
        color: #555;
        margin-top: 15px;
    }
</style>

<body>

    <div class="search-section">
        <div class="search-box">
            <div class="tabs">
                <div class="tab active">🔍 Search</div>
                <div class="tab">🌍 Destinations</div>
                <div class="tab">🏞️ Super Deals</div>
                <div class="tab">🌟 Featured</div>
            </div>

            <div class="fields">
                <div class="field">
                    <label>From City</label>
                    <input type="text" placeholder="Enter departure city" value="Patna" />
                </div>
                <div class="field">
                    <label>To City/Country/Category</label>
                    <input type="text" placeholder="Enter destination" value="Goa" />
                </div>
                <div class="field">
                    <label>Departure Date</label>
                    <input type="date" />
                </div>
                <div class="field">
                    <label>Rooms & Guests</label>
                    <select>
                        <option>Select Rooms</option>
                        <option>1 Room, 2 Guests</option>
                        <option>2 Rooms, 4 Guests</option>
                    </select>
                </div>
                <div class="field">
                    <label>Filters (Optional)</label>
                    <select>
                        <option>Select Filters</option>
                        <option>Student Discount</option>
                        <option>Senior Citizen</option>
                    </select>
                </div>
            </div>
            <div class="search-btn">
                <button>SEARCH</button>
            </div>
        </div>
    </div>

    <!-- Your Existing Card Row -->
    <!-- Goa -->
    <div class="card-row">
        <div class="card">
            <img src="https://th.bing.com/th/id/OIP.RGpdb3FKmZ07rSFIvoaEtAHaE8?rs=1&pid=ImgDetMain" alt="Destination"
                class="card-img">
            <div class="card-content">
                <h3>Goa, India</h3>
                <p>3 Nights, 4 Days • 2 Guests</p>
                <p class="price">₹7,999 / person</p>
                <button class="book-btn">Book Now</button>
            </div>
        </div>

        <!-- Manali -->

        <div class="card">
            <img src="https://th.bing.com/th/id/OIP.RGpdb3FKmZ07rSFIvoaEtAHaE8?rs=1&pid=ImgDetMain" alt="Destination"
                class="card-img">
            <div class="card-content">
                <h3>Manali, India</h3>
                <p>4 Nights, 5 Days • 2 Guests</p>
                <p class="price">₹9,499 / person</p>
                <button class="book-btn">Book Now</button>
            </div>
        </div>

        <!-- Kashmir -->

        <div class="card">
            <img src="https://www.holidify.com/images/bgImages/KASHMIR.jpg" alt="Kashmir" class="card-img">
            <div class="card-content">
                <h3>Kashmir, India</h3>
                <p>5 Nights, 6 Days • 2 Guests</p>
                <p class="price">₹11,999 / person</p>
                <button class="book-btn">Book Now</button>
            </div>
        </div>

        <!-- Kerala -->

        <div class="card">
            <img src="https://www.holidify.com/images/bgImages/KERALA.jpg" alt="Kerala" class="card-img">
            <div class="card-content">
                <h3>Kerala, India</h3>
                <p>4 Nights, 5 Days • 2 Guests</p>
                <p class="price">₹10,499 / person</p>
                <button class="book-btn">Book Now</button>
            </div>
        </div>

        <!-- Kathmandu -->

        <div class="card">
            <img src="https://www.holidify.com/images/bgImages/KATHMANDU.jpg" alt="Kathmandu" class="card-img">
            <div class="card-content">
                <h3>Kathmandu, Nepal</h3>
                <p>3 Nights, 4 Days • 2 Guests</p>
                <p class="price">₹8,999 / person</p>
                <button class="book-btn">Book Now</button>
            </div>
        </div>
        <!-- Shimla -->

        <div class="card">
            <img src="https://th.bing.com/th/id/OIP.RGpdb3FKmZ07rSFIvoaEtAHaE8?rs=1&pid=ImgDetMain" alt="Destination"
                class="card-img">
            <div class="card-content">
                <h3>Shimla, India</h3>
                <p>2 Nights, 3 Days • 2 Guests</p>
                <p class="price">₹6,299 / person</p>
                <button class="book-btn">Book Now</button>
            </div>
        </div>
    </div>
    <!-- FAQs -->

    <h3>Holiday Booking FAQs</h3>
    <div class="faq-container">
        <div class="faq-item">
            <div class="faq-question">What are the benefits of booking a holiday package online?</div>
            <div class="faq-answer">
                Online holiday booking offers convenience, customizable itineraries, exclusive discounts, and access to
                verified reviews and photos, all in one place.
            </div>
        </div>
        <div class="faq-item">
            <div class="faq-question">How early should I book a holiday package?</div>
            <div class="faq-answer">
                For the best prices and availability, book your holiday package at least 1–2 months in advance,
                especially during peak travel seasons.
            </div>
        </div>
        <div class="faq-item">
            <div class="faq-question">How do I book a holiday package online?</div>
            <div class="faq-answer">
                Select your destination, travel dates, number of travelers, and preferences. Then choose from available
                packages, customize if needed, and make a secure payment to confirm.
            </div>
        </div>
        <div class="faq-item">
            <div class="faq-question">What documents are required for holiday bookings?</div>
            <div class="faq-answer">
                For domestic holidays, a valid ID proof is required at check-ins. For international travel, you'll need
                a valid passport, visa, and any other country-specific documentation.
            </div>
        </div>
        <div class="faq-item">
            <div class="faq-question">Why book holiday packages through Goibibo?</div>
            <div class="faq-answer">
                Goibibo offers curated holiday packages, expert assistance, best price guarantees, GoCash benefits, 24/7
                customer support, and easy customization options.
            </div>
        </div>
        <div class="faq-item">
            <div class="faq-question">Can I customize or cancel my holiday package?</div>
            <div class="faq-answer">
                Yes, most holiday packages can be customized or canceled, subject to terms and conditions. Always check
                the package policy before booking.
            </div>
        </div>
        <!-- Coorg Video Section -->
        <div class="holiday-video-container">
            <h3>Discover Coorg – The Scotland of India</h3>
            <div class="holiday-video-item">
                <iframe width="800" height="450" src="https://www.youtube.com/embed/YdpJVGI1ZMw" frameborder="0"
                    allowfullscreen></iframe>
            </div>
            <div class="holiday-video-details">
                <p>Explore the lush landscapes, serene coffee plantations, and vibrant culture of Coorg. This video
                    offers a glimpse into the enchanting beauty of this hill station in Karnataka.</p>
            </div>
        </div>
        <b>&copy; 2025 Coorg Tour|All rights reserved</b>
        <!-- Shimla Video Section -->
        <div class="holiday-video-container">
            <h3>Discover Kashmir– The Queen of India</h3>
            <div class="holiday-video-item">
                <iframe width="700" height="400" src="https://www.youtube.com/embed/i253PPOaJs0?start=4" frameborder="0"
                    allowfullscreen></iframe>

            </div>
            <div class="holiday-video-details">
                <p>Explore the lush landscapes, serene coffee plantations, and vibrant culture of Kashmir. This video
                    offers a glimpse into the enchanting beauty of this hill station in Karnataka.</p>
            </div>
        </div>
        <b>&copy; 2025 Kashmir Tour|All rights reserved</b>


        <!-- Manali Video Section -->
        <div class="holiday-video-container">
            <h3>Discover Manali – A Paradise in the Himalayas</h3>
            <div class="holiday-video-item">
                <iframe width="800" height="450" src="https://www.youtube.com/embed/-8-ryNxd_Rg" frameborder="0"
                    allowfullscreen></iframe>
            </div>
            <div class="holiday-video-details">
                <p>Immerse yourself in the beauty of snow-capped mountains, lush green valleys, and adventure activities
                    in Manali. This video takes you on a journey through one of India's most loved hill stations.</p>
            </div>
        </div>
        <b>&copy; 2025 Manalli Tour|All rights reserved</b>
        <script src="Holidays.js"></script>
</body>

</html>
document.addEventListener("DOMContentLoaded", function () {
    document.querySelector(".search-btn button").addEventListener("click", function () {
        const fromCity = document.querySelector("input[placeholder='Enter departure city']").value.trim();
        const toCity = document.querySelector("input[placeholder='Enter destination']").value.trim();
        const departureDate = document.querySelector("input[type='date']").value.trim();
        const roomsGuests = document.querySelector("select:first-of-type").value.trim();

        // Validation for empty fields
        if (!fromCity || !toCity || !departureDate || roomsGuests === "Select Rooms") {
            alert("Please fill in all required fields before searching.");
            return;
        }

        // Example alert for search results (replace with actual functionality)
        alert(`Searching holidays from ${fromCity} to ${toCity} on ${departureDate} for ${roomsGuests}`);
    });
});
const bookButtons = document.querySelectorAll('.book-btn');

bookButtons.forEach(button => {
    button.addEventListener('click', () => {
        const card = button.closest('.card');
        const destination = card.querySelector('h3').innerText;
        const price = card.querySelector('.price').innerText;

        alert(`🎉 Booking confirmed!\nDestination: ${destination}\nPrice: ${price}`);
    });
});
body {
    font-family: Arial, sans-serif;
    margin: 0;
    padding: 20px;
    background-color: #971b1b;
}

form {
    max-width: 500px;
    margin: 0 auto;
    background-color: #fff;
    padding: 20px;
    border: 1px solid #ddd;
    border-radius: 10px;
    box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
}

div {
    margin-bottom: 20px;
    /* Spacing between each field */
}

label {
    display: block;
    font-weight: bold;
    margin-bottom: 8px;
    color: #333;
}

input[type="text"],
input[type="date"],
input[type="number"],
select {
    width: 100%;
    padding: 10px;
    border: 1px solid #ccc;
    border-radius: 5px;
    box-sizing: border-box;
    font-size: 14px;
    cursor: pointer;
}

input[type="text"]:focus,
input[type="date"]:focus,
input[type="number"]:focus,
select:focus {
    border-color: #007BFF;
    outline: none;
}

button {
    background-color: #007BFF;
    color: white;
    border: none;
    padding: 12px 20px;
    border-radius: 5px;
    cursor: pointer;
    font-size: 16px;
    width: 100%;
    transition: background-color 0.3s ease;
}

button:hover {
    background-color: #0056b3;
}

/* Additional spacing for better layout on mobile */
@media (max-width: 768px) {
    form {
        padding: 15px;
    }

    input[type="text"],
    input[type="date"],
    input[type="number"],
    select {
        font-size: 12px;
    }

    button {
        font-size: 14px;
        padding: 10px 16px;
    }
}



/* Headings */
h3 {
    text-align: center;
    margin: 30px 0;
    font-size: 24px;
    color: #ff1010;
}

/* Form Section */
.form-container {
    /* background-color: #397539; */
    background-color: rgb(139, 43, 43);
    padding: 25px;
    border-radius: 10px;
    box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
    max-width: 800px;
    margin: auto;
}

.faq-container{
    background-color: blueviolet;
}

fieldset {
    border: none;
}

legend {
    font-size: 20px;
    font-weight: 600;
    margin-bottom: 10px;
}

.form-content {
    display: flex;
    flex-wrap: wrap;
    gap: 20px;
    align-items: center;
}

.form-group {
    flex: 1 1 250px;
    display: flex;
    flex-direction: column;
}

label {
    margin-bottom: 5px;
    font-weight: 500;
}

input,
select {
    padding: 10px;
    border: 1px solid #ccc;
    border-radius: 8px;
    font-size: 16px;
    transition: 0.3s ease;
}

input:focus,
select:focus {
    border-color: #007bff;
    outline: none;
}

/* Basic styling for the container */
body {
    font-family: Arial, sans-serif;
    margin: 0;
    padding: 0;
    background-color: #f5f5f5;
}

div {
    margin-bottom: 15px;
    padding: 10px;
}

label {
    display: block;
    font-weight: bold;
    margin-bottom: 5px;
    color: #333;
}

input[type="text"],
input[type="date"],
input[type="number"] {
    width: 100%;
    padding: 8px;
    margin-top: 3px;
    border: 1px solid #ccc;
    border-radius: 5px;
    box-sizing: border-box;
    cursor: pointer;
}

/* Styling for the button */
#searchButton {
    background-color: #007BFF;
    color: white;
    border: none;
    padding: 10px 20px;
    border-radius: 5px;
    cursor: pointer;
    font-size: 16px;
    transition: background-color 0.3s ease;
}

#searchButton:hover {
    background-color: #0056b3;
}

/* Add a responsive layout */
@media (max-width: 768px) {

    input[type="text"],
    input[type="date"],
    input[type="number"] {
        font-size: 14px;
    }

    #searchButton {
        font-size: 14px;
        padding: 8px 16px;
    }
}


/* FAQ Section */
.faq-container {
    max-width: 800px;
    margin: 30px auto;
    /* background-color: #397539; */
    border-radius: 10px;
    padding: 25px;
    box-shadow: 0 4px 12px rgba(0, 0, 0, 0.08);
}

.faq-item {
    margin-bottom: 20px;
}

.faq-question {
    font-weight: 600;
    color: #2c3e50;
    cursor: pointer;
    margin-bottom: 5px;
}

.faq-answer {
    padding-left: 10px;
    color: #f1e9e9;
}

/* Footer Section */
.footer-box {
    background-color: #1f1f1f;
    color: #ccc;
    padding: 50px 20px 30px;
    margin-top: 50px;
    font-size: 15px;
}

.footer-container {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
    gap: 30px;
    max-width: 1200px;
    margin: auto;
}

.footer-column h3 {
    color: #63d485;
    margin-bottom: 15px;
    font-size: 16px;
}

.footer-column ul {
    list-style: none;
}

.footer-column ul li {
    margin-bottom: 10px;
}

.footer-column ul li a {
    text-decoration: none;
    color: #aaa;
    transition: color 0.3s;
}

.footer-column ul li a:hover {
    color: #ffffff;
}

/* Footer Bottom Section */
.last {
    text-align: center;
    margin-top: 40px;
}

.social-icons a {
    display: inline-block;
    color: #ccc;
    margin: 0 10px;
    font-size: 20px;
    transition: color 0.3s;
}

.social-icons a:hover {
    color: #ffffff;
}

.store-icons {
    margin: 15px 0;
}

.store-icons a {
    display: inline-block;
    margin: 10px;
}

.payment-icons {
    margin-top: 20px;
    font-size: 26px;
    color: #aaa;
}

.payment-icons i {
    margin: 0 10px;
    transition: color 0.3s;
}

.payment-icons i:hover {
    color: #fff;
}

.site-footer {
    margin-top: 30px;
    text-align: center;
    font-size: 14px;
    color: #777;
}

hr {
    border: 0;
    border-top: 1px solid #444;
    margin: 30px auto;
    max-width: 90%;
}

/* Responsive */
@media (max-width: 768px) {
    .form-content {
        flex-direction: column;
    }

    .form-group {
        width: 100%;
    }

    .faq-container {
        padding: 20px;
    }

    .footer-container {
        grid-template-columns: 1fr 1fr;
    }
}

@media (max-width: 480px) {
    .footer-container {
        grid-template-columns: 1fr;
        text-align: center;
    }

    .store-icons a img {
        width: 100px;
    }
}

.site-footer {
    background-color: #f4f4f4;
    padding: 40px 20px 20px;
    font-family: Arial, sans-serif;
    font-size: 14px;
    color: #333;
}

.footer-top {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
    gap: 20px;
    border-bottom: 1px solid #ccc;
    padding-bottom: 30px;
}

.footer-column h4 {
    font-weight: bold;
    margin-bottom: 10px;
}

.footer-column ul {
    list-style-type: none;
    padding: 0;
}

.footer-column ul li {
    margin-bottom: 6px;
    cursor: pointer;
}

.footer-bottom {
    display: flex;
    flex-wrap: wrap;
    justify-content: space-between;
    align-items: center;
    padding-top: 20px;
}

.social-icons,
.download-apps,
.payment-icons {
    margin: 10px 0;
}

.social-icons img,
.payment-icons img {
    width: 32px;
    margin-right: 10px;
}

.app-badge {
    height: 40px;
    margin-right: 10px;
}
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Airline Reservation System - Hotel Booking</title>
    <link rel="stylesheet" href="Common.css" />
    <link rel="stylesheet" href="Hotels.css">
    <link rel="stylesheet" href="Domestic Hotels.css">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.0/css/all.min.css" />
</head>


<body>
    <h3>Book Hotels and Homestays</h3>
    <form id="flightForm">
        <fieldset>
            <legend>Trip Details</legend>
            <div class="form-content">
                <div class="form-group">
                    <div>
                        <label for="sourceInput">Where to:</label>
                        <input type="text" id="sourceInput" placeholder="Enter location">
                        <!-- <label for="sourceInput">Destination:</label>
                            <input type="text" id="sourceInput" placeholder="Enter location"> -->
                    </div>
                    <div>
                        <label for="checkInDateInput">Check-in Date:</label>
                        <input type="date" id="checkInDateInput">
                    </div>
                    <div>
                        <label for="checkOutDateInput">Check-out Date:</label>
                        <input type="date" id="checkOutDateInput">
                    </div>
                    <div class="form-group">
                        <label for="travellers">Guests & Rooms:</label>
                        <input type="number" value="1" min="1" id="travellers" name="travellers" required />
                    </div>
                    <button id="searchButton">Search</button>
                </div>
        </fieldset>
    </form>
    </div>

    <h3>Hotel Booking FAQs</h3>
    <div class="faq-container">
        <div class="faq-item">
            <div class="faq-question">What are the advantages of online hotel booking?</div>
            <div class="faq-answer">
                Online hotel booking lets you compare prices, read reviews, check amenities, and book rooms from the
                comfort of your home.
            </div>
        </div>
        <div class="faq-item">
            <div class="faq-question">When is the best time to book hotels for the lowest prices?</div>
            <div class="faq-answer">
                For the best prices, try to book hotels at least 1–2 weeks in advance for domestic stays and 3–4 weeks
                for international destinations.
            </div>
        </div>
        <div class="faq-item">
            <div class="faq-question">How can I book hotels online?</div>
            <div class="faq-answer">
                Choose your destination, travel dates, and number of guests on an online platform. Filter options,
                select a hotel, and confirm your booking in a few clicks.
            </div>
        </div>
        <div class="faq-item">
            <div class="faq-question">What documents are required at the time of hotel check-in?</div>
            <div class="faq-answer">
                Most hotels require a valid government-issued photo ID (like Aadhar Card, Passport, Voter ID, or Driving
                License) for check-in. International travelers may need a passport and visa.
            </div>
        </div>
        <div class="faq-item">
            <div class="faq-question">Can I modify or cancel my hotel booking?</div>
            <div class="faq-answer">
                Yes, most hotels allow modifications or cancellations within a certain period. Always check the
                cancellation policy before booking.
            </div>
        </div>
        <div class="faq-item">
            <div class="faq-question">Are there any benefits of booking hotels through Goibibo?</div>
            <div class="faq-answer">
                Goibibo offers exclusive deals, GoCash benefits, verified reviews, and multiple payment options
                including UPI, cards, wallets, and net banking.
            </div>
        </div>
    </div>

    <!-- Footer Section Starts -->
    <footer class="site-footer">
        <div class="footer-top">
            <div class="footer-column">
                <h4>OUR PRODUCTS</h4>
                <ul>
                    <li>Domestic Hotels</li>
                    <li>International Hotels</li>
                    <li>International Flights</li>
                    <li>Bus Booking</li>
                    <li>Cab Booking</li>
                    <li>Train Ticket Booking</li>
                    <li>Route Planner</li>
                    <li>Cheap Flights</li>
                    <li>Hotels near me</li>
                    <li>Popular Airlines</li>
                </ul>
            </div>
            <div class="footer-column">
                <h4>COMPANY</h4>
                <ul>
                    <li>About Us</li>
                    <li>Privacy</li>
                    <li>Careers</li>
                    <li>Customer Support</li>
                    <li>FAQs</li>
                </ul>
            </div>
            <div class="footer-column">
                <h4>TRENDING HOTEL CITIES</h4>
                <ul>
                    <li>Hotels in Goa</li>
                    <li>Hotels in Delhi</li>
                    <li>Hotels in Mumbai</li>
                    <li>Hotels in Bangalore</li>
                    <li>Hotels in Chennai</li>
                </ul>
            </div>
            <div class="footer-column">
                <h4>TRENDING INTERNATIONAL HOTEL CITIES</h4>
                <ul>
                    <li>Hotels in Dubai</li>
                    <li>Hotels in Singapore</li>
                    <li>Hotels in London</li>
                    <li>Hotels in New York</li>
                    <li>Hotels in Paris</li>
                </ul>
            </div>
            <div class="footer-column">
                <h4>TOP SEARCHED HOTELS BY AREA</h4>
                <ul>
                    <li>Hotels in Panchgani</li>
                    <li>Hotels in Shirdi</li>
                    <li>Hotels in Ooty</li>
                    <li>Hotels in Manali</li>
                    <li>Hotels in Lonavala</li>
                </ul>
            </div>
            <div class="footer-column">
                <h4>ALTERNATE ACCOMMODATION IN CITY</h4>
                <ul>
                    <li>Homestays in Coorg</li>
                    <li>Homestays in Ooty</li>
                    <li>Homestays in Manali</li>
                    <li>Villas in Goa</li>
                    <li>Villas in Lonavala</li>
                </ul>
            </div>
            <div class="footer-column">
                <h4>TOP 5 STAR HOTEL CITIES</h4>
                <ul>
                    <li>5 Star Hotels in Delhi</li>
                    <li>5 Star Hotels in Mumbai</li>
                    <li>5 Star Hotels in Goa</li>
                    <li>5 Star Hotels in Chennai</li>
                    <li>5 Star Hotels in Kolkata</li>
                </ul>
            </div>
        </div>

        <div class="footer-bottom">
            <div class="social-icons">
                <span>Follow Us</span>
                <a href="https://www.facebook.com/YourPage" target="_blank">
                    <img src="https://img.icons8.com/ios-filled/24/facebook--v1.png" />
                </a>
                <a href="https://twitter.com/YourProfile" target="_blank">
                    <img src="https://img.icons8.com/ios-filled/24/twitter--v1.png" />
                </a>
                <a href="https://www.instagram.com/YourProfile" target="_blank">
                    <img src="https://img.icons8.com/ios-filled/24/instagram-new.png" />
                </a>

            </div>
            <div class="download-apps">
                <span>Download our Mobile Apps</span>
                <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/7/78/Google_Play_Store_badge_EN.svg/2560px-Google_Play_Store_badge_EN.svg.png"
                    alt="Play Store" class="app-badge">
                <img src="https://developer.apple.com/assets/elements/badges/download-on-the-app-store.svg"
                    alt="App Store" class="app-badge">
            </div>
            <div class="payment-icons">
                <img src="https://img.icons8.com/color/48/visa.png" />
                <img src="https://img.icons8.com/color/48/mastercard-logo.png" />
                <img src="https://img.icons8.com/color/48/rupay.png" />
                <img src="https://img.icons8.com/color/48/paypal.png" />
            </div>
        </div>
    </footer>
    <script src="Hotels.js"></script>
</body>

</html>
document.addEventListener("DOMContentLoaded", function () {
    // Event listener for the hotel search button
    const searchButton = document.querySelector("#searchButton");

    // Check if the button exists
    if (searchButton) {
        searchButton.addEventListener("click", function () {
            // Get input values
            const location = document.querySelector("#sourceInput").value.trim();
            const checkInDate = document.querySelector("#checkInDateInput").value.trim();
            const checkOutDate = document.querySelector("#checkOutDateInput").value.trim();
            const guestsAndRooms = document.querySelector("#travellers").value.trim();

            // Validation for empty fields
            if (!location || !checkInDate || !checkOutDate || guestsAndRooms < 1) {
                alert("Please fill in all required fields before searching.");
                return;
            }

            // Simulated search result (replace with real functionality later)
            alert(`Searching hotels in ${location} from ${checkInDate} to ${checkOutDate} for ${guestsAndRooms} guests.`);
        });
    } else {
        console.error("The hotel search button with ID 'searchButton' was not found.");
    }
});
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Countries Filter by Alphabet</title>
    <link rel="stylesheet" href="style1.css" />
</head>

<body>
    <div class="container">
        <h1>Search Countries by Letter!</h1>

        <div class="alphabet-buttons">
            <!-- A-Z buttons here -->
        </div>

        <div class="search-bar">
            <input type="text" id="searchInput" placeholder="Type to search country..." />
            <p id="listeningStatus" class="listening-text" style="display: none;">🎧 Listening...</p>
        </div>

        <div class="dropdown">
            <select id="countryList">
                <option value="">Select a country</option>
                <!-- Countries populated here -->
            </select>
        </div>
        <div class="search-bar">
            <input type="text" id="searchInput" placeholder="Type to search country..." />
            <button id="micBtn" title="Speak" class="mic-button">🎤</button>
        </div>

    </div>

    <script src="script2.js"></script>
</body>

</html>
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Login</title>
    <!-- <link rel="stylesheet" href="Login.css">
    <link rel="stylesheet" href="SignUp.css"> -->
    <link rel="stylesheet" href="styleAir.css">
</head>
<style>
    * {
        margin: 0;
        padding: 0;
        box-sizing: border-box;
    }

    body {
        font-family: Arial, sans-serif;
        background-color: #386bc0;
        display: flex;
        justify-content: center;
        align-items: center;
        height: 100vh;
    }

    .login-container {
        background-color: #fff;
        padding: 30px;
        border-radius: 8px;
        box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
        width: 100%;
        max-width: 400px;
        box-sizing: border-box;
    }

    h2 {
        text-align: center;
        margin-bottom: 20px;
        color: #333;
    }

    .input-group {
        margin-bottom: 15px;
    }

    .input-group label {
        display: block;
        font-weight: bold;
        color: #555;
    }

    .input-group input {
        width: 100%;
        padding: 10px;
        border: 1px solid #ccc;
        border-radius: 4px;
        font-size: 16px;
        color: #333;
    }

    .input-group input:focus {
        border-color: #0066cc;
        outline: none;
    }

    .btn {
        width: 100%;
        padding: 12px;
        background-color: #0066cc;
        border: none;
        border-radius: 4px;
        font-size: 16px;
        color: white;
        cursor: pointer;
        transition: background-color 0.3s;
    }

    .btn:hover {
        background-color: #005bb5;
    }

    .signup-link {
        text-align: center;
        margin-top: 15px;
    }

    .signup-link a {
        color: #0066cc;
        text-decoration: none;
    }

    .signup-link a:hover {
        text-decoration: underline;
    }

    .footer {
        text-align: center;
        margin-top: 30px;
        font-weight: bold;
        color: #333;
    }
</style>
<script src="Login.js"></script>
<script src="SignUp.js"></script>

<body>
    <div class="login-container">
        <form class="login-form" autocomplete="off">
            <h2>Login</h2>
            <div class="input-group">
                <label for="email">Email</label>
                <input type="email" id="email" autocomplete="off" name="email" placeholder="Enter your email" required>
            </div>
            <div class="input-group">
                <label for="password">Password</label>
                <input type="password" id="password" autocomplete="new-password" name="password"
                    placeholder="Enter your password" required>
            </div>
            <button type="submit" class="btn">Login</button>
            <div class="signup-link">
                <p>Already have an account? <a href="SignUp.html">SignUp</a></p>
            </div>
        </form>
    </div>
    <!-- Place this inside <body>, after the login container -->

</body>

</html>
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

body {
    font-family: Arial, sans-serif;
    background-color: #386bc0;
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100vh;
}

.login-container {
    background-color: #fff;
    padding: 30px;
    border-radius: 8px;
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
    width: 100%;
    max-width: 400px;
    box-sizing: border-box;
}

h2 {
    text-align: center;
    margin-bottom: 20px;
    color: #333;
}

.input-group {
    margin-bottom: 15px;
}

.input-group label {
    display: block;
    font-weight: bold;
    color: #555;
}

.input-group input {
    width: 100%;
    padding: 10px;
    border: 1px solid #ccc;
    border-radius: 4px;
    font-size: 16px;
    color: #333;
}

.input-group input:focus {
    border-color: #0066cc;
    outline: none;
}

.btn {
    width: 100%;
    padding: 12px;
    background-color: #0066cc;
    border: none;
    border-radius: 4px;
    font-size: 16px;
    color: white;
    cursor: pointer;
    transition: background-color 0.3s;
}

.btn:hover {
    background-color: #005bb5;
}

.signup-link {
    text-align: center;
    margin-top: 15px;
}

.signup-link a {
    color: #0066cc;
    text-decoration: none;
}

.signup-link a:hover {
    text-decoration: underline;
}
.footer {
    text-align: center;
    margin-top: 30px;
    font-weight: bold;
    color: #333;
}
document.addEventListener("DOMContentLoaded", function () {
    const loginForm = document.querySelector(".login-form");

    loginForm.addEventListener("submit", function (event) {
        event.preventDefault(); // Prevent form submission to handle validation

        // Get form values
        const email = document.getElementById("email").value.trim();
        const password = document.getElementById("password").value.trim();

        // Simple validation checks
        if (!email || !password) {
            alert("Please fill out both fields.");
            return;
        }

        if (!validateEmail(email)) {
            alert("Please enter a valid email address.");
            return;
        }

      
        // Show success message
        alert("🎉 Login successful!");

        // ✅ Clear the form after success
        loginForm.reset();

        // Optional: redirect to another page
        window.location.href = "thankyou.html";
    });

    function validateEmail(email) {
        const regex = /^[^\s@]+@[^\s@]+\.[^\s@]+$/;
        return regex.test(email);
    }
});
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Sign Up</title>
    <!-- <link rel="stylesheet" href="SignUp.css"> -->
    <link rel="stylesheet" href="styleAir.css">
    <script src="SignUp.js"></script>
</head>
<style>
    body {
        font-family: Arial, sans-serif;
        background: #1565c0;
        margin: 0;
        padding: 0;
        display: flex;
        align-items: center;
        justify-content: center;
        height: 100vh;
    }

    .signup-container {
        background: white;
        padding: 30px 40px;
        border-radius: 10px;
        box-shadow: 0 8px 20px rgba(0, 0, 0, 0.1);
        width: 350px;
        text-align: center;
    }

    h2 {
        margin-bottom: 20px;
        color: #333;
    }

    label {
        display: block;
        text-align: left;
        margin: 10px 0 5px;
        font-weight: bold;
    }

    input[type="text"],
    input[type="email"],
    input[type="password"] {
        width: 100%;
        padding: 10px;
        border: 1px solid #ccc;
        border-radius: 6px;
        box-sizing: border-box;
    }

    button {
        width: 100%;
        padding: 12px;
        background-color: #0066d9;
        border: none;
        color: white;
        font-size: 16px;
        margin-top: 20px;
        border-radius: 6px;
        cursor: pointer;
    }

    button:hover {
        background-color: #004caa;
    }

    p {
        margin-top: 15px;
        font-size: 14px;
    }

    a {
        color: #0066d9;
        text-decoration: none;
    }

    a:hover {
        text-decoration: underline;
    }
</style>

<body>

    <div class="signup-container">
        <h2>Create Account</h2>
        <form id="signup-form">
            <label for="name">Name</label>
            <input type="text" id="name" placeholder="Enter your name" required>

            <label for="email">Email</label>
            <input type="email" id="email" placeholder="Enter your email" required>

            <label for="password">Password</label>
            <input type="password" id="password" placeholder="Enter your password" required>

            <label for="confirm-password">Confirm Password</label>
            <input type="password" id="confirm-password" placeholder="Confirm your password" required>

            <button type="submit">Sign Up</button>
        </form>
        <p>Already have an account? <a href="login.html">Login</a></p>
    </div>

</body>

</html>
body {
    font-family: Arial, sans-serif;
    background: #1565c0;
    margin: 0;
    padding: 0;
    display: flex;
    align-items: center;
    justify-content: center;
    height: 100vh;
}

.signup-container {
    background: white;
    padding: 30px 40px;
    border-radius: 10px;
    box-shadow: 0 8px 20px rgba(0, 0, 0, 0.1);
    width: 350px;
    text-align: center;
}

h2 {
    margin-bottom: 20px;
    color: #333;
}

label {
    display: block;
    text-align: left;
    margin: 10px 0 5px;
    font-weight: bold;
}

input[type="text"],
input[type="email"],
input[type="password"] {
    width: 100%;
    padding: 10px;
    border: 1px solid #ccc;
    border-radius: 6px;
    box-sizing: border-box;
}

button {
    width: 100%;
    padding: 12px;
    background-color: #0066d9;
    border: none;
    color: white;
    font-size: 16px;
    margin-top: 20px;
    border-radius: 6px;
    cursor: pointer;
}

button:hover {
    background-color: #004caa;
}

p {
    margin-top: 15px;
    font-size: 14px;
}

a {
    color: #0066d9;
    text-decoration: none;
}

a:hover {
    text-decoration: underline;
}
document.getElementById("signup-form").addEventListener("submit", function (event) {
    event.preventDefault();

    const name = document.getElementById("name").value;
    const email = document.getElementById("email").value;
    const password = document.getElementById("password").value;
    const confirmPassword = document.getElementById("confirm-password").value;

    if (password !== confirmPassword) {
        alert("Passwords do not match.");
        return;
    }

    // Simulate successful signup
    alert("Account created successfully!");
    // You can redirect or send this data to your backend here
    // Example: window.location.href = "login.html";
});
body {
    margin: 0;
    font-family: Arial, sans-serif;
  }
  
  /* Modal Styles */
  .modal {
    display: none;
    position: fixed;
    z-index: 999;
    left: 0;
    top: 0;
    width: 100%;
    height: 100%;
    overflow: auto;
    background-color: rgba(0,0,0,0.6);
  }
  
  .modal-content {
    background-color: #fff;
    margin: 10% auto;
    padding: 0;
    border: none;
    border-radius: 10px;
    width: 90%;
    max-width: 400px;
    position: relative;
  }
  
  .close-btn {
    position: absolute;
    top: 8px;
    right: 12px;
    font-size: 28px;
    font-weight: bold;
    color: #333;
    cursor: pointer;
  }
  <!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Thank You</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background: linear-gradient(to right, #83a4d4, #b6fbff);
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            margin: 0;
        }
        .message-box {
            background: white;
            padding: 40px;
            border-radius: 12px;
            box-shadow: 0 0 20px rgba(0,0,0,0.1);
            text-align: center;
            font-size: 1.5rem;
        }
    </style>
</head>
<body>
    <div class="message-box" id="thankYouMsg"></div>

    <script>
        const msg = sessionStorage.getItem("thankYouMessage");
        document.getElementById("thankYouMsg").textContent = msg || "🎉 Thank you! Visit again soon.!";
        sessionStorage.removeItem("thankYouMessage"); // optional: clear after showing
    </script>
</body>
</html>
document.addEventListener("DOMContentLoaded", function () {
    // Event listener for the train search button
    const searchButton = document.querySelector("#trainSearchButton");
    searchButton.addEventListener("click", function () {
        // Get input values
        const fromStation = document.querySelector("#trainSourceInput").value.trim();
        const toStation = document.querySelector("#trainDestinationInput").value.trim();
        const journeyDate = document.querySelector("#trainDateInput").value.trim();
        const trainClass = document.querySelector("#trainClass").value.trim(); // Fixed selector

        // Validation for empty fields
        if (!fromStation || !toStation || !journeyDate || !trainClass) {
            alert("Please fill in all required fields before searching.");
            return;
        }

        // Simulated search result (replace with real functionality later)
        alert(`Searching trains from ${fromStation} to ${toStation} on ${journeyDate} in ${trainClass} class.`);
    });
});
/* Global Styles */
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-family: "Segoe UI", sans-serif;
}

body {
    background-color: #f7f9fc;
    color: #333;
    line-height: 1.6;
    padding: 20px;
    background-image: url('https://roadlesstravelled.me/wp-content/uploads/2017/01/worlds-best-train-journeys.jpg');
    background-size: cover;
    background-repeat: no-repeat;
    background-attachment: fixed;
}

/* Headings */
h3 {
    text-align: center;
    margin: 30px 0;
    font-size: 24px;
    color: #2c3e50;
}

/* Form Section */
.form-container {
    background-color: #397539;
    padding: 25px;
    border-radius: 10px;
    box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
    max-width: 800px;
    margin: auto;
}

fieldset {
    border: none;
}

legend {
    font-size: 20px;
    font-weight: 600;
    margin-bottom: 10px;
}

.form-content {
    display: flex;
    flex-wrap: wrap;
    gap: 20px;
    align-items: center;
}

.form-group {
    flex: 1 1 250px;
    display: flex;
    flex-direction: column;
}

label {
    margin-bottom: 5px;
    font-weight: 500;
}

input,
select {
    padding: 10px;
    border: 1px solid #ccc;
    border-radius: 8px;
    font-size: 16px;
    margin: 12px;
    transition: 0.3s ease;
}

input:focus,
select:focus {
    border-color: #007bff;
    outline: none;
}

button#searchBtn1 {
    padding: 12px 20px;
    background-color: #ff0000;
    color: #244824;
    border: none;
    border-radius: 8px;
    font-size: 16px;
    cursor: pointer;
    transition: background 0.3s;
    margin-left: 18rem;
    margin-right: 18rem;
}

button#searchBtn1:hover {
    background-color: #0056b3;
}

/* FAQ Section */
.faq-container {
    max-width: 800px;
    margin: 30px auto;
    background-color:  #397539;
    border-radius: 10px;
    padding: 25px;
    box-shadow: 0 4px 12px rgba(0, 0, 0, 0.08);
}

.faq-item {
    margin-bottom: 20px;
}

.faq-question {
    font-weight: 600;
    color: #2c3e50;
    cursor: pointer;
    margin-bottom: 5px;
}

.faq-answer {
    padding-left: 10px;
    color:#f1e9e9;
}

/* Footer Section */
.footer-box {
    background-color: #1f1f1f;
    color: #ccc;
    padding: 50px 20px 30px;
    margin-top: 50px;
    font-size: 15px;
}

.footer-container {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
    gap: 30px;
    max-width: 1200px;
    margin: auto;
}

.footer-column h3 {
    color: #63d485;
    margin-bottom: 15px;
    font-size: 16px;
}

.footer-column ul {
    list-style: none;
}

.footer-column ul li {
    margin-bottom: 10px;
}

.footer-column ul li a {
    text-decoration: none;
    color: #aaa;
    transition: color 0.3s;
}

.footer-column ul li a:hover {
    color: #ffffff;
}

/* Footer Bottom Section */
.last {
    text-align: center;
    margin-top: 40px;
}

.social-icons a {
    display: inline-block;
    color: #ccc;
    margin: 0 10px;
    font-size: 20px;
    transition: color 0.3s;
}

.social-icons a:hover {
    color: #ffffff;
}

.store-icons {
    margin: 15px 0;
}

.store-icons a {
    display: inline-block;
    margin: 10px;
}

.payment-icons {
    margin-top: 20px;
    font-size: 26px;
    color: #aaa;
}

.payment-icons i {
    margin: 0 10px;
    transition: color 0.3s;
}

.payment-icons i:hover {
    color: #fff;
}

.site-footer {
    margin-top: 30px;
    text-align: center;
    font-size: 14px;
    color: #777;
}

hr {
    border: 0;
    border-top: 1px solid #444;
    margin: 30px auto;
    max-width: 90%;
}

/* Responsive */
@media (max-width: 768px) {
    .form-content {
        flex-direction: column;
    }

    .form-group {
        width: 100%;
    }

    .faq-container {
        padding: 20px;
    }

    .footer-container {
        grid-template-columns: 1fr 1fr;
    }
}

@media (max-width: 480px) {
    .footer-container {
        grid-template-columns: 1fr;
        text-align: center;
    }

    .store-icons a img {
        width: 100px;
    }
}

.site-footer {
    background-color: #f4f4f4;
    padding: 40px 20px 20px;
    font-family: Arial, sans-serif;
    font-size: 14px;
    color: #333;
}

.footer-top {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
    gap: 20px;
    border-bottom: 1px solid #ccc;
    padding-bottom: 30px;
}

.footer-column h4 {
    font-weight: bold;
    margin-bottom: 10px;
}

.footer-column ul {
    list-style-type: none;
    padding: 0;
}

.footer-column ul li {
    margin-bottom: 6px;
    cursor: pointer;
}

.footer-bottom {
    display: flex;
    flex-wrap: wrap;
    justify-content: space-between;
    align-items: center;
    padding-top: 20px;
}

.social-icons,
.download-apps,
.payment-icons {
    margin: 10px 0;
}

.social-icons img,
.payment-icons img {
    width: 32px;
    margin-right: 10px;
}

.app-badge {
    height: 40px;
    margin-right: 10px;
}
body {
    font-family: Arial, sans-serif;
    margin: 0;
    padding: 20px;
    background-color: #f5f5f5;
}

.form-section {
    margin: 20px 0;
    padding: 20px;
    background: #fff;
    border: 1px solid #ddd;
    border-radius: 10px;
    box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
}

h2 {
    margin-bottom: 15px;
    font-size: 20px;
    color: #333;
}

label {
    display: block;
    font-weight: bold;
    margin-bottom: 5px;
    color: #333;
}

input[type="text"],
input[type="date"] {
    width: 100%;
    padding: 8px;
    margin-bottom: 15px;
    border: 1px solid #ccc;
    border-radius: 5px;
    box-sizing: border-box;
}

/* Container styling */
.form-container-horizontal {
    max-width: 800px;
    margin: 20px auto;
    background-color: #fff;
    padding: 20px;
    border-radius: 10px;
    box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
    border: 1px solid #ddd;
    font-family: Arial, sans-serif;
}

h2 {
    text-align: center;
    margin-bottom: 20px;
    font-size: 18px;
    color: #333;
}

/* Form row styling for horizontal alignment */
/* Styling for the form container */
.form-container-horizontal {
    max-width: 800px;
    margin: 20px auto;
    background-color: #fff;
    padding: 20px;
    border-radius: 10px;
    box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
    border: 1px solid #ddd;
    font-family: Arial, sans-serif;
}

/* Title styling */
h2 {
    text-align: center;
    margin-bottom: 20px;
    font-size: 18px;
    color: #333;
}

/* Form row for horizontal alignment */
.form-row {
    display: flex;
    justify-content: space-between;
    /* Ensures even spacing between elements */
    align-items: center;
    /* Aligns elements vertically */
    gap: 15px;
    /* Space between input fields and button */
    flex-wrap: wrap;
    /* Adjusts layout for smaller screens */
}

/* Individual form group styling */
.form-group {
    flex: 1;
    /* Makes fields flexible for proper alignment */
    min-width: 200px;
    /* Minimum width to ensure visibility */
}

label {
    display: block;
    font-weight: bold;
    margin-bottom: 5px;
    color: #333;
}

input[type="text"],
input[type="date"],
select {
    width: 100%;
    padding: 8px;
    font-size: 14px;
    border: 1px solid #ccc;
    border-radius: 5px;
    box-sizing: border-box;
}

/* Styling for the dropdown (train class) */
select {
    background-color: #f9f9f9;
}

/* Button styling */
button {
    flex: 0 1 auto;
    /* Adjusts button size without affecting fields */
    padding: 12px 20px;
    background-color: #007BFF;
    color: #fff;
    border: none;
    border-radius: 5px;
    cursor: pointer;
    font-size: 16px;
    transition: background-color 0.3s ease;
}

button:hover {
    background-color: #0056b3;
}

/* Responsive adjustments */
@media (max-width: 768px) {
    .form-row {
        flex-direction: column;
        /* Stacks fields vertically on smaller screens */
    }

    button {
        width: 100%;
        /* Makes the button full width on small screens */
    }
}
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Airline Reservation System - Train Ticket Booking</title>
    <link rel="stylesheet" href="Common.css">
    <link rel="stylesheet" href="Trains.css">
    <script src="train.js"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.0/css/all.min.css" />
</head>


<body>
    <h3>Book Train Tickets</h3>
    <div class="form-container-horizontal">
        <h2>Train Ticket Booking</h2>
        <div class="form-row">
            <div class="form-group">
                <label for="trainSourceInput">From:</label>
                <input type="text" id="trainSourceInput" placeholder="Enter source station">
            </div>
            <div class="form-group">
                <label for="trainDestinationInput">To:</label>
                <input type="text" id="trainDestinationInput" placeholder="Enter destination station">
            </div>
            <div class="form-group">
                <label for="trainDateInput">Date:</label>
                <input type="date" id="trainDateInput">
            </div>
            <div class="form-group">
                <label for="trainClass">Class:</label>
                <select id="trainClass">
                    <option value="sleeper">Sleeper</option>
                    <option value="ac1">AC 1</option>
                    <option value="ac2">AC 2</option>
                    <option value="ac3">AC 3</option>
                </select>
            </div>
            <button id="trainSearchButton">Search Trains</button>
        </div>
    </div>
    </fieldset>
    </form>

    <!-- Results Placeholder -->
    <div id="trainResults"></div>
    </div>

    <!-- FAQs Section -->
    <h3>Train Booking FAQs</h3>
    <div class="faq-container">
        <div class="faq-item">
            <div class="faq-question">What are the advantages of online train booking?</div>
            <div class="faq-answer">
                Online train booking allows you to compare routes, check seat availability, access deals, and book
                tickets conveniently from home.
            </div>
        </div>
        <div class="faq-item">
            <div class="faq-question">When should I book to get the best train ticket availability?</div>
            <div class="faq-answer">
                It's best to book train tickets as early as possible, ideally when the booking window opens—usually 120
                days in advance for most trains.
            </div>
        </div>
        <div class="faq-item">
            <div class="faq-question">How can I book train tickets online?</div>
            <div class="faq-answer">
                You can book train tickets online via platforms like IRCTC or travel portals. Enter your journey
                details, select a train and class, and make the payment to confirm your ticket.
            </div>
        </div>
        <div class="faq-item">
            <div class="faq-question">What documents are required for online train ticket booking & can I make changes
                in my train booking?</div>
            <div class="faq-answer">
                During online train ticket booking, no documents are needed. However, during travel, carry a valid photo
                ID like Aadhar Card, Voter ID, Driving License, or PAN Card. IRCTC doesn't allow changes to booked
                tickets—you must cancel and rebook.
            </div>
        </div>
        <div class="faq-item">
            <div class="faq-question">Why book train tickets online through Goibibo?</div>
            <div class="faq-answer">
                Goibibo provides a user-friendly booking experience, great deals, GoCash benefits, and flexible payment
                options such as UPI, cards, wallets, and net banking.
            </div>
        </div>
        <div class="faq-item">
            <div class="faq-question">What other railway services does Goibibo offer?</div>
            <div class="faq-answer">
                Besides ticket booking, Goibibo allows you to check PNR status, live train status, recover IRCTC login
                details, cancel tickets, and more.
            </div>
        </div>
    </div>
    <!-- Footer Section -->
    <footer class="site-footer">
        <div class="footer-top">
            <div class="footer-column">
                <h4>OUR PRODUCTS</h4>
                <ul>
                    <li>Domestic Hotels</li>
                    <li>International Hotels</li>
                    <li>International Flights</li>
                    <li>Bus Booking</li>
                    <li>Cab Booking</li>
                    <li>Train Ticket Booking</li>
                    <li>Route Planner</li>
                    <li>Cheap Flights</li>
                    <li>Hotels near me</li>
                    <li>Popular Airlines</li>
                </ul>
            </div>
            <div class="footer-column">
                <h4>COMPANY</h4>
                <ul>
                    <li>About Us</li>
                    <li>Privacy</li>
                    <li>Careers</li>
                    <li>Customer Support</li>
                    <li>FAQs</li>
                </ul>
            </div>
            <div class="footer-column">
                <h4>TRENDING HOTEL CITIES</h4>
                <ul>
                    <li>Hotels in Goa</li>
                    <li>Hotels in Delhi</li>
                    <li>Hotels in Mumbai</li>
                    <li>Hotels in Bangalore</li>
                    <li>Hotels in Chennai</li>
                </ul>
            </div>
            <div class="footer-column">
                <h4>TRENDING INTERNATIONAL HOTEL CITIES</h4>
                <ul>
                    <li>Hotels in Dubai</li>
                    <li>Hotels in Singapore</li>
                    <li>Hotels in London</li>
                    <li>Hotels in New York</li>
                    <li>Hotels in Paris</li>
                </ul>
            </div>
            <div class="footer-column">
                <h4>TOP SEARCHED HOTELS BY AREA</h4>
                <ul>
                    <li>Hotels in Panchgani</li>
                    <li>Hotels in Shirdi</li>
                    <li>Hotels in Ooty</li>
                    <li>Hotels in Manali</li>
                    <li>Hotels in Lonavala</li>
                </ul>
            </div>
            <div class="footer-column">
                <h4>ALTERNATE ACCOMMODATION IN CITY</h4>
                <ul>
                    <li>Homestays in Coorg</li>
                    <li>Homestays in Ooty</li>
                    <li>Homestays in Manali</li>
                    <li>Villas in Goa</li>
                    <li>Villas in Lonavala</li>
                </ul>
            </div>
            <div class="footer-column">
                <h4>TOP 5 STAR HOTEL CITIES</h4>
                <ul>
                    <li>5 Star Hotels in Delhi</li>
                    <li>5 Star Hotels in Mumbai</li>
                    <li>5 Star Hotels in Goa</li>
                    <li>5 Star Hotels in Chennai</li>
                    <li>5 Star Hotels in Kolkata</li>
                </ul>
            </div>
        </div>

        <div class="footer-bottom">
            <div class="download-apps">
                <span>Download our Mobile Apps</span>
                <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/7/78/Google_Play_Store_badge_EN.svg/2560px-Google_Play_Store_badge_EN.svg.png"
                    alt="Play Store" class="app-badge" />
                <img src="https://developer.apple.com/assets/elements/badges/download-on-the-app-store.svg"
                    alt="App Store" class="app-badge" />
            </div>
            <div class="payment-icons">
                <img src="https://img.icons8.com/color/48/visa.png" />
                <img src="https://img.icons8.com/color/48/mastercard-logo.png" />
                <img src="https://img.icons8.com/color/48/rupay.png" />
                <img src="https://img.icons8.com/color/48/paypal.png" />
            </div>
        </div>
    </footer>
</body>

</html>
