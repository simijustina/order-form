<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Online Order Form</title>
    <style>
        body { 
            font-family: Arial, sans-serif; 
            background-color: #f4f8f9; 
            color: #333; 
            margin: 0; 
            padding: 0;
        }
        .container { 
            max-width: 600px; 
            margin: auto; 
            padding: 20px; 
            border: 1px solid #ccc; 
            border-radius: 10px; 
            background-color: #ffffff; 
            box-shadow: 0 2px 15px rgba(0, 0, 0, 0.1);
        }
        h1, h2 {
            color: #18ac91; /* Theme color */
            text-align: center;
        }
        .form-group {
            margin-bottom: 20px;
        }
        label {
            display: block;
            margin-bottom: 5px;
            font-weight: bold;
        }
        input[type="email"],
        input[type="tel"],
        input[type="text"],
        input[type="number"],
        select,
        textarea {
            width: 100%;
            padding: 10px;
            border: 1px solid #ccc;
            border-radius: 5px;
            box-sizing: border-box; /* Include padding and border in the element's total width */
        }
        input[type="email"]:focus,
        input[type="tel"]:focus,
        input[type="text"]:focus,
        input[type="number"]:focus,
        select:focus,
        textarea:focus {
            border-color: #0ba6e3; /* Highlight border on focus */
            outline: none; /* Remove default outline */
        }
        .medication-section {
            margin-bottom: 30px; /* Add space below medication section */
            padding: 15px;
            border: 1px solid #0998fe;
            border-radius: 10px;
            background-color: #0485b72f; /* Light background for medication section */
        }
        button { 
            margin-top: 10px; 
            background-color: #0ba6e3; /* Theme button color */
            color: white; 
            border: none; 
            padding: 10px 15px; 
            border-radius: 5px; 
            cursor: pointer; 
            width: 100%; /* Full width button */
            font-size: 16px; /* Larger font size */
        }
        button:hover { 
            background-color: #f00606; /* Darker shade on hover */
        }
        @media (max-width: 768px) {
            .container {
                padding: 15px;
            }
        }
        @media (max-width: 480px) {
            h1 {
                font-size: 1.5em;
            }
            h2 {
                font-size: 1.2em;
            }
        }
    </style>
    <script>
        function calculateTotal() {
            const medications = document.querySelectorAll('.medication');
            let total = 0;

            medications.forEach(med => {
                const price = parseFloat(med.querySelector('.price').value);
                const quantity = parseInt(med.querySelector('.quantity').value);
                total += price * quantity;
            });

            const discountCode = document.getElementById('discountCode').value;
            if (discountCode === "DISCMED40" && total > 100) {
                total -= 40; // Apply discount
            }

            total = total < 0 ? 0 : total; // Ensure total doesn't go negative
            document.getElementById('totalPrice').innerText = 'Total Price: $' + total.toFixed(2);
        }

        function setDefaultQuantity(selectElement) {
            const quantityInput = selectElement.parentElement.querySelector('.quantity');
            if (selectElement.value !== "0") {
                quantityInput.value = 1; // Set default quantity to 1 when a medication is selected
            } else {
                quantityInput.value = 0; // Reset quantity if no medication is selected
            }
            calculateTotal(); // Recalculate total when medication is selected
        }

        function prepareEmailData(event) {
            event.preventDefault(); // Prevent default form submission

            const formData = {
                email: document.getElementById('email').value,
                phone: document.getElementById('phone').value,
                address: document.getElementById('address').value,
                discountCode: document.getElementById('discountCode').value,
                totalPrice: document.getElementById('totalPrice').innerText,
                medications: []
            };

            const medications = document.querySelectorAll('.medication');
            medications.forEach(med => {
                const selectedMedication = med.querySelector('select').value;
                const quantity = med.querySelector('.quantity').value;
                if (selectedMedication !== "0" && quantity > 0) {
                    const medicationName = med.querySelector('select option:checked').textContent;
                    formData.medications.push(`${medicationName}: Quantity ${quantity}`);
                }
            });

            // Convert formData to a string for email
            const emailBody = `
                Email: ${formData.email}
                Phone: ${formData.phone}
                Address: ${formData.address}
                Discount Code: ${formData.discountCode}
                Total Price: ${formData.totalPrice}
                Medications: ${formData.medications.join(', ')}
            `;

            // Send data to Formspree
            fetch('https://formspree.io/f/xjkyekor', {
                method: 'POST',
                headers: {
                    'Content-Type': 'application/json'
                },
                body: JSON.stringify({ message: emailBody })
            })
            .then(response => {
                if (response.ok) {
                    alert('Order submitted successfully!');
                    document.querySelector('form').reset(); // Reset the form
                    calculateTotal(); // Reset total price
                } else {
                    alert('There was an error submitting your order. Please try again.');
                }
            })
            .catch(error => {
                console.error('Error:', error);
                alert('There was an error submitting your order. Please try again.');
            });
        }
    </script>
</head>
<body>
    <div class="container">
        <h1>The MedExpress Online Order Form</h1>
        
        <form onsubmit="prepareEmailData(event)">
            <div class="medication-section">
                <h2>Medication Selection</h2>
                <div class="medication form-group">
                    <label for="med1">MOUNJARO:</label>
                    <select class="price" onchange="setDefaultQuantity(this)" name="Mounjaro">
                        <option value="0">Select Medication</option>
                        <option value="150">Mounjaro 2.5mg - $150</option>
                        <option value="180">Mounjaro 5mg - $180</option>
                        <option value="200">Mounjaro 7.5mg - $200</option>
                        <option value="330">Mounjaro 10mg - $330</option>
                        <option value="400">Mounjaro 12.5mg - $400</option>
                        <option value="420">Mounjaro 15mg - $420</option>
                    </select>
                    <input type="number" class="quantity" value="0" min="0" onchange="calculateTotal()" placeholder="Quantity" name="quantity1">
                </div>
                <div class="medication form-group">
                    <label for="med2">WEGOVY</label>
                    <select class="price" onchange="setDefaultQuantity(this)" name="med2">
                        <option value="0">Select Medication</option>
                        <option value="200">Wegovy 0.25mg - $200</option>
                        <option value="235">Wegovy 0.5mg - $235</option>
                        <option value="265">Wegovy 1mg - $265</option>
                        <option value="295">Wegovy 1.7mg - $295</option>
                        <option value="350">Wegovy 2.4mg - $350</option>
                    </select>
                    <input type="number" class="quantity" value="0" min="0" onchange="calculateTotal()" placeholder="Quantity" name="quantity2">
                </div>
                <div class="medication form-group">
                    <label for="med3">OZEMPIC:</label>
                    <select class="price" onchange="setDefaultQuantity(this)" name="med3">
                        <option value="0">Select Medication</option>
                        <option value="350">Ozempic 1mg - $350</option>
                        <option value="300">Ozempic 0.5mg - $300</option>
                        <option value="250">Ozempic 0.25mg  - $250</option>
                    </select>
                    <input type="number" class="quantity" value="0" min="0" onchange="calculateTotal()" placeholder="Quantity" name="quantity3">
                </div>
                <div class="medication form-group">
                    <label for="med4">SAXENDER:</label>
                    <select class="price" onchange="setDefaultQuantity(this)" name="med4">
                        <option value="0">Select Medication</option>
                        <option value="350">Saxender 5 pens - $350</option>
                        <option value="200">Saxender 3 pens - $200</option>
                    </select>
                    <input type="number" class="quantity" value="0" min="0" onchange="calculateTotal()" placeholder="Quantity" name="quantity4">
                </div>
                <div class="medication form-group">
                    <label for="med5">ACXION:</label>
                    <select class="price" onchange="setDefaultQuantity(this)" name="med5">
                        <option value="0">Select Medication</option>
                        <option value="75">Acxion AP 30mg - $75</option>
                        <option value="65">Acxion 30mg - $65</option>
                    </select>
                    <input type="number" class="quantity" value="0" min="0" onchange="calculateTotal()" placeholder="Quantity" name="quantity5">
                </div>
                <div class="medication form-group">
                    <label for="med6">OTHER MEDICATIONS:</label>
                    <select class="price" onchange="setDefaultQuantity(this)" name="med6">
                        <option value="0">Select Medication</option>
                        <option value="70">Terfamex - $70</option>
                        <option value="75">Adipex 37.5mg (30tbl) - $75</option>
                        <option value="100">Duromine 30mg - $100</option>
                        <option value="55">Norex - $55</option>
                        <option value="60">ASibrutril 15mg - $60</option>
                    </select>
                    <input type="number" class="quantity" value="0" min="0" onchange="calculateTotal()" placeholder="Quantity" name="quantity6">
                </div>
            </div>

            <div class="form-group">
                <label for="email">Email:</label>
                <input type="email" id="email" name="email" required placeholder="Enter your email">
            </div>
            <div class="form-group">
                <label for="phone">Phone Number:</label>
                <input type="tel" id="phone" name="phone" required placeholder="Enter your phone number">
            </div>
            <div class="form-group">
                <label for="country">Country:</label>
                <select id="country" name="country" required>
                    <option value="">Select Your Country</option>
                    <option value="US">United States</option>
                    <option value="CA">Canada</option>
                    <option value="GB">United Kingdom</option>
                    <option value="AU">Australia</option>
                    <option value="IN">India</option>
                    <option value="DE">Germany</option>
                    <option value="FR">France</option>
                    <option value="JP">Japan</option>
                    <option value="CN">China</option>
                    <option value="BR">Brazil</option>
                    <!-- Add more countries as needed -->
                </select>
            </div>
            <div class="form-group">
                <label for="address">Shipping Address:</label>
                <textarea id="address" name="address" required placeholder="Enter your shipping address"></textarea>
            </div>

            <h2 id="totalPrice">Total Price: $0.00</h2>
            <div class="form-group">
                <label for="discountCode">Discount Code:</label>
                <input type="text" id="discountCode" oninput="calculateTotal()" placeholder="Enter discount code" name="discountCode">
            </div>
            <div>
                <h6>We shall confirm your order by email and you will pay before we complete your order for shipping.</h6>
            </div>
            <button type="submit">Submit Order</button>
        </form>
    </div>
</body>
</html>
