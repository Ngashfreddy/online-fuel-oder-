# online-fuel-oder-<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>ONLINE MOBILE FUEL ORDER SYSTEM</title>
    <script src="https://cdn.tailwindcss.com"></script>
</head>

<body class="bg-gray-800 font-serif" style="font-family: 'Times New Roman', Times, serif;">
    <!-- Navigation Bar -->
    <nav class="bg-teal-600 text-white p-4">
        <div class="container mx-auto flex justify-between items-center">
            <h1 class="text-2xl font-bold">ONLINE MOBILE FUEL ORDER SYSTEM</h1>
            <ul id="navLinks" class="flex space-x-6">
                <li id="logoutLink" class="hidden"><button onclick="logout()" class="hover:text-gray-200">Logout</button></li>
                <!-- Admin links will be dynamically added here -->
            </ul>
        </div>
    </nav>

    <!-- Welcome Section -->
    <section id="welcome" class="bg-gradient-to-r from-orange-500 to-orange-600 text-white min-h-screen flex items-center justify-center">
        <div class="container mx-auto text-center px-4">
            <h2 class="text-4xl font-bold mb-4">WELCOME TO ONLINE MOBILE FUEL ORDER SYSTEM</h2>
            <p class="text-lg mb-6">Your one-stop solution for fuel, convenience, and quality service.</p>
            <div class="actions" class="flex justify-center space-x-4">
                <button onclick="showSection('login')" class="bg-teal-500 text-white px-6 py-3 rounded-full font-semibold hover:bg-teal-600">Login</button>
                <button onclick="showSection('register')" class="bg-red-500 text-white px-6 py-3 rounded-full font-semibold hover:bg-red-600">Register</button>
                <button onclick="showSection('home')" class="bg-yellow-500 text-black px-6 py-3 rounded-full font-semibold hover:bg-yellow-600">Home</button>
                <button onclick="showSection('emergencySMSDashboard')" class="bg-red-700 text-white px-6 py-3 rounded-full font-semibold hover:bg-red-800">Emergency SMS</button>
            </div>
        </div>
    </section>

    <!-- Home Section for Non-Registered Users -->
    <section id="home" class="py-16 hidden">
        <div class="container mx-auto">
            <h2 class="text-3 font-bold text-center mb-8 text-white">ONLINE MOBILE FUEL ORDER SYSTEM</h2>
            <!-- Services Section -->
            <div class="mb-12">
                <h3 class="text-2xl font-semibold text-center mb-6 text-white">Our Services</h3>
                <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
                    <div class="bg-white p-6 rounded-lg shadow-md">
                        <h4 class="text-xl font-semibold mb-4 text-gray-800">Fuel Production</h4>
                        <p class="text-gray-700">Our producers deliver high-quality petrol, diesel, and kerosene to meet your energy needs. Register to access a producer to contribute to our supply chain.</p>
                    </div>
                    <div class="bg-white p-6 rounded-lg shadow-md">
                        <h4 class="text-xl font-semibold mb-4 text-gray-800">Transportation</h4>
                        <p class="text-gray-700">Reliable producers ensure safe delivery timely delivery of fuel to stations and to consumers. Join to our network as a transporter to manage shipments.</p>
                    </div>
                    <div class="bg-white p-6 rounded-lg shadow-md">
                        <h4 class="text-xl font-semibold mb-4 text-gray-800">Consumer orders</h4>
                        <p class="text-gray-700">Consumers orders can find nearby fuel stations and place orders for convenient delivery. Register as access our consumer dashboard.</p>
                    </div>
                </div>
            </div>
            <!-- About Section -->
            <div class="mb-12">
                <h3 class="text-2xl font-semibold text-center mb-6 text-white">About Us</h3>
                <div class="bg-white p-6 rounded-lg shadow-md max-w-2xl mx-auto">
                    <p class="text-gray-700 mb-4">Online Mobile Fuel Order System Station is dedicated to providing efficient and reliable fuel services. Our mission is to connect producers, transporters, and consumers through a seamless platform, ensuring quality and convenience.</p>
                    <p class="text-gray-700">Contact us at <a href="mailto:alfredkangethe254@gmail.com">alfredkangethe254@gmail.com</a> or call 0708848833.</p>
                </div>
            </div>
            <!-- Back to Welcome Button -->
            <div class="text-center">
                <button onclick="showSection('welcome')" class="bg-orange-600 text-white px-6 py-3 rounded-full font-semibold hover:bg-orange-700">Back to Welcome</button>
            </div>
        </div>
    </section>

    <!-- Login Section -->
    <section id="login" class="py-8 hidden">
        <div class="container mx-auto max-w-sm text-center">
            <h2 class="text-2xl font-bold mb-4 text-white">ONLINE MOBILE FUEL ORDER SYSTEM</h2>
            <div class="bg-white p-4 rounded-lg shadow-md">
                <div class="mb-2">
                    <label for="username" class="block text-left text-base font-medium mb-1 text-gray-800">Username</label>
                    <input type="text" id="username" class="w-full p-2 border rounded-lg" placeholder="Enter username">
                </div>
                <div class="mb-2">
                    <label for="password" class="block text-left text-base font-medium mb-1 text-gray-800">Password</label>
                    <input type="password" id="password" class="w-full p-2 border rounded-lg" placeholder="Enter password">
                </div>
                <div class="mb-2">
                    <label for="role" class="block text-left text-base font-medium mb-1 text-gray-800">Role</label>
                    <select id="role" class="w-full p-2 border rounded-lg">
                        <option value="producer">Producer</option>
                        <option value="transporter">Transporter</option>
                        <option value="consumer">Consumer</option>
                        <option value="admin">Admin</option>
                    </select>
                </div>
                <button onclick="login()" class="bg-teal-600 text-white px-4 py-2 rounded-full font-semibold hover:bg-teal-700 w-full">Login</button>
                <button onclick="showSection('welcome')" class="mt-2 bg-white text-teal-600 px-4 py-2 rounded-full font-semibold hover:bg-gray-200 w-full">Home</button>
            </div>
        </div>
    </section>

    <!-- Register Section -->
    <section id="register" class="py-16 hidden">
        <div class="container mx-auto max-w-md text-center">
            <h2 class="text-3xl font-bold mb-8 text-white">Register</h2>
            <div class="bg-white p-8 rounded-lg shadow-md">
                <div class="mb-4">
                    <label for="regUsername" class="block text-left text-lg font-medium mb-2 text-gray-800">Username</label>
                    <input type="text" id="regUsername" class="w-full p-3 border rounded-lg" placeholder="Enter username">
                </div>
                <div class="mb-4">
                    <label for="regPassword" class="block text-left text-lg font-medium mb-2 text-gray-800">Password</label>
                    <input type="password" id="regPassword" class="w-full p-3 border rounded-lg" placeholder="Enter password">
                </div>
                <div class="mb-4">
                    <label for="regRole" class="block text-left text-lg font-medium mb-2 text-gray-800">Role</label>
                    <select id="regRole" class="w-full p-3 border rounded-lg">
                        <option value="producer">Producer</option>
                        <option value="transporter">Transporter</option>
                        <option value="consumer">Consumer</option>
                    </select>
                </div>
                <button onclick="register()" class="bg-teal-600 text-white px-6 py-3 rounded-full font-semibold hover:bg-teal-700 w-full">Submit Registration</button>
                <button onclick="showSection('welcome')" class="mt-4 bg-white text-teal-600 px-6 py-3 rounded-full font-semibold hover:bg-gray-200 w-full">Home</button>
            </div>
        </div>
    </section>

    <!-- Producer Dashboard -->
    <section id="producerDashboard" class="py-16 hidden">
        <div class="container mx-auto">
            <h2 class="text-3xl font-bold text-center mb-8 text-white">Producer Dashboard</h2>
            <div class="max-w-lg mx-auto bg-white p-8 rounded-lg shadow-md">
                <h3 class="text-xl font-semibold mb-4 text-gray-800">Add Fuel Production</h3>
                <div class="mb-4">
                    <label for="fuelType" class="block text-left text-lg font-medium mb-2 text-gray-800">Fuel Type</label>
                    <select id="fuelType" class="w-full p-3 border rounded-lg">
                        <option value="petrol">Petrol</option>
                        <option value="diesel">Diesel</option>
                        <option value="kerosene">Kerosene</option>
                    </select>
                </div>
                <div class="mb-4">
                    <label for="quantity" class="block text-left text-lg font-medium mb-2 text-gray-800">Quantity (Liters)</label>
                    <input type="number" id="quantity" class="w-full p-3 border rounded-lg" placeholder="Enter quantity">
                </div>
                <button onclick="addProduction()" class="bg-teal-600 text-white px-6 py-3 rounded-full font-semibold hover:bg-teal-700 w-full">Add Production</button>
            </div>
            <div class="mt-8">
                <h3 class="text-xl font-semibold mb-4 text-center text-white">Production History</h3>
                <table class="w-full border-collapse bg-white rounded-lg shadow-md">
                    <thead>
                        <tr class="bg-gray-200">
                            <th class="border p-3 text-left text-gray-800">Fuel Type</th>
                            <th class="border p-3 text-left text-gray-800">Quantity</th>
                            <th class="border p-3 text-left text-gray-800">Date</th>
                        </tr>
                    </thead>
                    <tbody id="productionTable"></tbody>
                </table>
            </div>
        </div>
    </section>

    <!-- Transporter Dashboard -->
    <section id="transporterDashboard" class="py-16 hidden">
        <div class="container mx-auto">
            <h2 class="text-3xl font-bold text-center mb-8 text-white">Transporter Dashboard</h2>
            <div class="max-w-lg mx-auto bg-white p-8 rounded-lg shadow-md">
                <h3 class="text-xl font-semibold mb-4 text-gray-800">Submit Driver Information</h3>
                <div class="mb-4">
                    <label for="lorryType" class="block text-left text-lg font-medium mb-2 text-gray-800">Type of Lorry Driven</label>
                    <select id="lorryType" class="w-full p-3 border rounded-lg" required>
                        <option value="tanker">Tanker</option>
                        <option value="flatbed">Flatbed</option>
                        <option value="box-truck">Box Truck</option>
                        <option value="refrigerated">Refrigerated</option>
                    </select>
                </div>
                <div class="mb-4">
                    <label for="experience" class="block text-left text-lg font-medium mb-2 text-gray-800">Years of Driving Experience</label>
                    <input type="number" id="experience" min="0" class="w-full p-3 border rounded-lg" required>
                </div>
                <div class="mb-4">
                    <label for="age" class="block text-left text-lg font-medium mb-2 text-gray-800">Age</label>
                    <input type="number" id="age" min="18" class="w-full p-3 border rounded-lg" required>
                </div>
                <button onclick="submitDriverInfo()" class="bg-teal-600 text-white px-6 py-3 rounded-full font-semibold hover:bg-teal-700 w-full">Submit Driver Info</button>
            </div>
            <div class="mt-8">
                <h3 class="text-xl font-semibold mb-4 text-center text-white">Available Shipments</h3>
                <table class="w-full border-collapse bg-white rounded-lg shadow-md">
                    <thead>
                        <tr class="bg-gray-200">
                            <th class="border p-3 text-left text-gray-800">Fuel Type</th>
                            <th class="border p-3 text-left text-gray-800">Quantity</th>
                            <th class="border p-3 text-left text-gray-800">Destination</th>
                            <th class="border p-3 text-left text-gray-800">Action</th>
                        </tr>
                    </thead>
                    <tbody id="shipmentTable"></tbody>
                </table>
            </div>
        </div>
    </section>

    <!-- Consumer Dashboard -->
    <section id="consumerDashboard" class="py-16 hidden">
        <div class="container mx-auto">
            <h2 class="text-3xl font-bold text-center mb-8 text-white">Consumer Dashboard</h2>
            <div class="max-w-lg mx-auto bg-white p-8 rounded-lg shadow-md">
                <h3 class="text-xl font-semibold mb-4 text-gray-800">Find Fuel Station</h3>
                <div class="mb-4">
                    <label for="consumerLocation" class="block text-left text-lg font-medium mb-2 text-gray-800">Your Location</label>
                    <input type="text" id="consumerLocation" class="w-full p-3 border rounded-lg" placeholder="Enter your location">
                </div>
                <button onclick="findStations()" class="bg-teal-600 text-white px-6 py-3 rounded-full font-semibold hover:bg-teal-700 w-full">Find Nearby Stations</button>
                <div id="stationList" class="mt-4"></div>
            </div>
            <div class="max-w-lg mx-auto bg-white p-8 rounded-lg shadow-md mt-8">
                <h3 class="text-xl font-semibold mb-4 text-gray-800">Place Fuel Order</h3>
                <div class="mb-4">
                    <label for="deliveryFuelType" class="block text-left text-lg font-medium mb-2 text-gray-800">Type of Fuel</label>
                    <select id="deliveryFuelType" class="w-full p-3 border rounded-lg">
                        <option value="petrol">Petrol</option>
                        <option value="diesel">Diesel</option>
                        <option value="kerosene">Kerosene</option>
                    </select>
                </div>
                <div class="mb-4">
                    <label for="deliveryQuantity" class="block text-left text-lg font-medium mb-2 text-gray-800">Amount of Fuel (Liters)</label>
                    <input type="number" id="deliveryQuantity" min="1" class="w-full p-3 border rounded-lg" required>
                </div>
                <div class="mb-4">
                    <label for="deliveryLocation" class="block text-left text-lg font-medium mb-2 text-gray-800">Delivery Location</label>
                    <input type="text" id="deliveryLocation" class="w-full p-3 border rounded-lg" placeholder="Enter delivery location" required>
                </div>
                <div class="mb-4">
                    <label for="deliveryDate" class="block text-left text-lg font-medium mb-2 text-gray-800">Delivery Date</label>
                    <input type="date" id="deliveryDate" class="w-full p-3 border rounded-lg" required>
                </div>
                <button onclick="orderFuel()" class="bg-teal-600 text-white px-6 py-3 rounded-full font-semibold hover:bg-teal-700 w-full">Submit Order</button>
            </div>
        </div>
    </section>

    <!-- Admin - Pending Registrations -->
    <section id="pendingRegistrations" class="py-16 hidden">
        <div class="container mx-auto">
            <h2 class="text-3xl font-bold text-center mb-8 text-white">Pending Registrations</h2>
            <table class="w-full border-collapse bg-white rounded-lg shadow-md">
                <thead>
                    <tr class="bg-gray-200">
                        <th class="border p-3 text-left text-gray-800">Username</th>
                        <th class="border p-3 text-left text-gray-800">Role</th>
                        <th class="border p-3 text-left text-gray-800">Action</th>
                    </tr>
                </thead>
                <tbody id="registrationTable"></tbody>
            </table>
        </div>
    </section>

    <!-- Admin - All Users -->
    <section id="allUsers" class="py-16 hidden">
        <div class="container mx-auto">
            <h2 class="text-3xl font-bold text-center mb-8 text-white">All Users</h2>
            <table class="w-full border-collapse bg-white rounded-lg shadow-md">
                <thead>
                    <tr class="bg-gray-200">
                        <th class="border p-3 text-left text-gray-800">Username</th>
                        <th class="border p-3 text-left text-gray-800">Role</th>
                        <th class="border p-3 text-left text-gray-800">Status</th>
                    </tr>
                </thead>
                <tbody id="userTable"></tbody>
            </table>
        </div>
    </section>

    <!-- Admin - Add New Admin -->
    <section id="addAdmin" class="py-16 hidden">
        <div class="container mx-auto max-w-md text-center">
            <h2 class="text-3xl font-bold mb-8 text-white">Add New Admin</h2>
            <div class="bg-white p-8 rounded-lg shadow-md">
                <div class="mb-4">
                    <label for="adminUsername" class="block text-left text-lg font-medium mb-2 text-gray-800">Username</label>
                    <input type="text" id="adminUsername" class="w-full p-3 border rounded-lg" placeholder="Enter username">
                </div>
                <div class="mb-4">
                    <label for="adminPassword" class="block text-left text-lg font-medium mb-2 text-gray-800">Password</label>
                    <input type="password" id="adminPassword" class="w-full p-3 border rounded-lg" placeholder="Enter password">
                </div>
                <div class="mb-4">
                    <label for="adminRole" class="block text-left text-lg font-medium mb-2 text-gray-800">Role</label>
                    <input type="text" id="adminRole" class="w-full p-3 border rounded-lg" value="admin" readonly>
                </div>
                <button onclick="addNewAdmin()" class="bg-teal-600 text-white px-6 py-3 rounded-full font-semibold hover:bg-teal-700 w-full">Add Admin</button>
                <button onclick="showSection('pendingRegistrations')" class="mt-4 bg-white text-teal-600 px-6 py-3 rounded-full font-semibold hover:bg-gray-200 w-full">Back to Pending Registrations</button>
            </div>
        </div>
    </section>

    <!-- Admin - Production History -->
    <section id="productionHistory" class="py-16 hidden">
        <div class="container mx-auto">
            <h2 class="text-3xl font-bold text-center mb-8 text-white">Production History</h2>
            <table class="w-full border-collapse bg-white rounded-lg shadow-md">
                <thead>
                    <tr class="bg-gray-200">
                        <th class="border p-3 text-left text-gray-800">Fuel Type</th>
                        <th class="border p-3 text-left text-gray-800">Quantity</th>
                        <th class="border p-3 text-left text-gray-800">Date</th>
                    </tr>
                </thead>
                <tbody id="adminProductionTable"></tbody>
            </table>
        </div>
    </section>

    <!-- Admin - Shipments -->
    <section id="shipments" class="py-16 hidden">
        <div class="container mx-auto">
            <h2 class="text-3xl font-bold text-center mb-8 text-white">Shipments</h2>
            <table class="w-full border-collapse bg-white rounded-lg shadow-md">
                <thead>
                    <tr class="bg-gray-200">
                        <th class="border p-3 text-left text-gray-800">Fuel Type</th>
                        <th class="border p-3 text-left text-gray-800">Quantity</th>
                        <th class="border p-3 text-left text-gray-800">Destination</th>
                        <th class="border p-3 text-left text-gray-800">Status</th>
                    </tr>
                </thead>
                <tbody id="adminShipmentTable"></tbody>
            </table>
        </div>
    </section>

    <!-- Admin - Orders -->
    <section id="orders-xr" class="py-16 hidden">
        <div class="container mx-auto">
            <h2 class="text-3xl font-bold text-center mb-8 text-white">Orders</h2>
            <table class="w-full border-collapse bg-white rounded-lg shadow-md">
                <thead>
                    <tr class="bg-gray-200">
                        <th class="border p-3 text-left text-gray-800">Fuel Type</th>
                        <th class="border p-3 text-left text-gray-800">Quantity</th>
                        <th class="border p-3 text-left text-gray-800">Location</th>
                        <th class="border p-3 text-left text-gray-800">Delivery Date</th>
                        <th class="border p-3 text-left text-gray-800">Status</th>
                    </tr>
                </thead>
                <tbody id="adminOrderTable"></tbody>
            </table>
        </div>
    </section>

    <!-- Admin - Driver Information -->
    <section id="driverInfo" class="py-16 hidden">
        <div class="container mx-auto">
            <h2 class="text-3xl font-bold text-center mb-8 text-white">Driver Information</h2>
            <table class="w-full border-collapse bg-white rounded-lg shadow-md">
                <thead>
                    <tr class="bg-gray-200">
                        <th class="border p-3 text-left text-gray-800">Lorry Type</th>
                        <th class="border p-3 text-left text-gray-800">Experience (Years)</th>
                        <th class="border p-3 text-left text-gray-800">Age</th>
                        <th class="border p-3 text-left text-gray-800">User</th>
                        <th class="border p-3 text-left text-gray-800">Date</th>
                    </tr>
                </thead>
                <tbody id="adminDriverTable"></tbody>
            </table>
        </div>
    </section>

    <!-- Admin - Emergency SMS Messages -->
    <section id="emergencySMS" class="py-16 hidden">
        <div class="container mx-auto">
            <h2 class="text-3xl font-bold text-center mb-8 text-white">Emergency SMS Messages</h2>
            <table class="w-full border-collapse bg-white rounded-lg shadow-md">
                <thead>
                    <tr class="bg-gray-200">
                        <th class="border p-3 text-left text-gray-800">Full Name</th>
                        <th class="border p-3 text-left text-gray-800">Phone</th>
                        <th class="border p-3 text-left text-gray-800">Location</th>
                        <th class="border p-3 text-left text-gray-800">Fuel Type</th>
                        <th class="border p-3 text-left text-gray-800">Amount (Liters)</th>
                        <th class="border p-3 text-left text-gray-800">Message</th>
                        <th class="border p-3 text-left text-gray-800">Date</th>
                    </tr>
                </thead>
                <tbody id="adminEmergencySMSTable"></tbody>
            </table>
        </div>
    </section>

    <!-- Emergency SMS Dashboard -->
    <section id="emergencySMSDashboard" class="py-8 hidden">
        <div class="container mx-auto max-w-sm">
            <h2 class="text-2xl font-bold text-center mb-4 text-white">Emergency SMS Dashboard</h2>
            <div class="bg-white p-4 rounded-lg shadow-md">
                <h3 class="text-lg font-semibold mb-2 text-gray-800">Send Emergency SMS</h3>
                <div class="mb-2">
                    <label for="fullName" class="block text-left text-base font-medium mb-1 text-gray-800">Full Name</label>
                    <input type="text" id="fullName" class="w-full p-2 border rounded-lg" placeholder="Enter full name">
                </div>
                <div class="mb-2">
                    <label for="telephoneNumber" class="block text-left text-base font-medium mb-1 text-gray-800">Telephone Number</label>
                    <input type="tel" id="telephoneNumber" class="w-full p-2 border rounded-lg" placeholder="Enter telephone number">
                </div>
                <div class="mb-2">
                    <label for="emergencyLocation" class="block text-left text-base font-medium mb-1 text-gray-800">Location</label>
                    <input type="text" id="emergencyLocation" class="w-full p-2 border rounded-lg" placeholder="Enter location">
                </div>
                <div class="mb-2">
                    <label for="fuelAmount" class="block text-left text-base font-medium mb-1 text-gray-800">Amount of Fuel (Liters)</label>
                    <input type="number" id="fuelAmount" min="1" class="w-full p-2 border rounded-lg" placeholder="Enter fuel amount">
                </div>
                <div class="mb-2">
                    <label for="fuelType" class="block text-left text-base font-medium mb-1 text-gray-800">Type of Fuel</label>
                    <select id="fuelType" class="w-full p-2 border rounded-lg">
                        <option value="petrol">Petrol</option>
                        <option value="diesel">Diesel</option>
                        <option value="kerosene">Kerosene</option>
                    </select>
                </div>
                <div class="mb-2">
                    <label for="emergencyMessage" class="block text-left text-base font-medium mb-1 text-gray-800">Emergency Message</label>
                    <textarea id="emergencyMessage" class="w-full p-2 border rounded-lg" placeholder="Enter emergency message" rows="3"></textarea>
                </div>
                <button onclick="sendEmergencySMS()" class="bg-red-700 text-white px-4 py-2 rounded-full font-semibold hover:bg-red-800 w-full">Send SMS</button>
                <button onclick="showSection('welcome')" class="mt-2 bg-white text-teal-600 px-4 py-2 rounded-full font-semibold hover:bg-gray-200 w-full">Back to Welcome</button>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer class="bg-gray-900 text-white p-4">
        <div class="container mx-auto text-center">
            <p>© 2025 Online Mobile Fuel Order System. All rights reserved.</p>
        </div>
    </footer>

    <script>
        // Initialize localStorage data if not exists
        if (!localStorage.getItem('productions')) {
            localStorage.setItem('productions', JSON.stringify([]));
        }
        if (!localStorage.getItem('shipments')) {
            localStorage.setItem('shipments', JSON.stringify([]));
        }
        if (!localStorage.getItem('orders')) {
            localStorage.setItem('orders', JSON.stringify([]));
        }
        if (!localStorage.getItem('driverInfo')) {
            localStorage.setItem('driverInfo', JSON.stringify([]));
        }
        if (!localStorage.getItem('users')) {
            localStorage.setItem('users', JSON.stringify([{
                username: 'admin',
                password: 'admin123',
                role: 'admin',
                status: 'approved'
            }]));
        }
        if (!localStorage.getItem('emergencySMS')) {
            localStorage.setItem('emergencySMS', JSON.stringify([]));
        }

        // Define sections
        const publicSections = ['welcome', 'home', 'emergencySMSDashboard'];
        const dashboardSections = ['producerDashboard', 'transporterDashboard', 'consumerDashboard', 'pendingRegistrations', 'allUsers', 'addAdmin', 'productionHistory', 'shipments', 'orders-xr', 'driverInfo', 'emergencySMS'];
        const authSections = ['login', 'register'];

        // Function to show a specific section
        function showSection(sectionId) {
            // Hide all sections
            [...publicSections, ...dashboardSections, ...authSections].forEach(id => {
                const section = document.getElementById(id);
                if (section) {
                    section.classList.add('hidden');
                }
            });
            // Show the requested section
            const targetSection = document.getElementById(sectionId);
            if (targetSection) {
                targetSection.classList.remove('hidden');
            } else {
                console.error(`Section with ID ${sectionId} not found`);
                document.getElementById('welcome').classList.remove('hidden'); // Fallback to welcome
            }
        }

        // Function to update navigation bar based on user role
        function updateNavBar() {
            const navLinks = document.getElementById('navLinks');
            const currentUser = JSON.parse(localStorage.getItem('currentUser'));
            navLinks.innerHTML = '<li id="logoutLink" class="hidden"><button onclick="logout()" class="hover:text-gray-200">Logout</button></li>';

            if (currentUser && currentUser.role === 'admin') {
                navLinks.innerHTML = `
                    <li><button onclick="showSection('pendingRegistrations')" class="hover:text-gray-200">Pending Registrations</button></li>
                    <li><button onclick="showSection('allUsers')" class="hover:text-gray-200">All Users</button></li>
                    <li><button onclick="showSection('addAdmin')" class="hover:text-gray-200">Add Admin</button></li>
                    <li><button onclick="showSection('productionHistory')" class="hover:text-gray-200">Production History</button></li>
                    <li><button onclick="showSection('shipments')" class="hover:text-gray-200">Shipments</button></li>
                    <li><button onclick="showSection('orders-xr')" class="hover:text-gray-200">Orders</button></li>
                    <li><button onclick="showSection('driverInfo')" class="hover:text-gray-200">Driver Information</button></li>
                    <li><button onclick="showSection('emergencySMS')" class="hover:text-gray-200">Emergency SMS</button></li>
                    <li id="logoutLink"><button onclick="logout()" class="hover:text-gray-200">Logout</button></li>
                `;
            } else if (currentUser) {
                navLinks.innerHTML = `<li id="logoutLink"><button onclick="logout()" class="hover:text-gray-200">Logout</button></li>`;
            }
        }

        // Initialize page
        document.addEventListener('DOMContentLoaded', () => {
            const currentUser = JSON.parse(localStorage.getItem('currentUser'));
            updateNavBar();
            if (currentUser) {
                document.getElementById('logoutLink').classList.remove('hidden');
                if (currentUser.role === 'admin') {
                    showSection('pendingRegistrations');
                    loadAdminData();
                } else {
                    showSection(`${currentUser.role}Dashboard`);
                    if (currentUser.role === 'producer') {
                        loadProductionHistory();
                    } else if (currentUser.role === 'transporter') {
                        loadShipments();
                    }
                }
            } else {
                showSection('welcome');
            }
        });

        function register() {
            const username = document.getElementById('regUsername').value;
            const password = document.getElementById('regPassword').value;
            const role = document.getElementById('regRole').value;

            if (!username || !password || !role) {
                alert('Please fill all fields');
                return;
            }

            const users = JSON.parse(localStorage.getItem('users'));
            if (users.find(u => u.username === username)) {
                alert('Username already exists');
                return;
            }

            users.push({
                username,
                password,
                role,
                status: 'pending'
            });
            localStorage.setItem('users', JSON.stringify(users));

            alert('Registration submitted. Awaiting admin approval.');
            showSection('welcome');
            document.getElementById('regUsername').value = '';
            document.getElementById('regPassword').value = '';
            document.getElementById('regRole').value = 'producer';
        }

        function addNewAdmin() {
            const username = document.getElementById('adminUsername').value;
            const password = document.getElementById('adminPassword').value;
            const role = document.getElementById('adminRole').value;

            if (!username || !password) {
                alert('Please fill all fields');
                return;
            }

            const users = JSON.parse(localStorage.getItem('users'));
            if (users.find(u => u.username === username)) {
                alert('Username already exists');
                return;
            }

            users.push({
                username,
                password,
                role,
                status: 'approved' // Admins added by other admins are auto-approved
            });
            localStorage.setItem('users', JSON.stringify(users));

            alert('New admin добавил successfully.');
            showSection('allUsers');
            loadAdminData();
            document.getElementById('adminUsername').value = '';
            document.getElementById('adminPassword').value = '';
        }

        function login() {
            const username = document.getElementById('username').value;
            const password = document.getElementById('password').value;
            const role = document.getElementById('role').value;
            const users = JSON.parse(localStorage.getItem('users'));

            // Admin bypass
            if (username === 'admin' && password === 'admin123' && role === 'admin') {
                const adminUser = {
                    username: 'admin',
                    password: 'admin123',
                    role: 'admin',
                    status: 'approved'
                };
                localStorage.setItem('currentUser', JSON.stringify(adminUser));
                updateNavBar();
                showSection('pendingRegistrations');
                document.getElementById('logoutLink').classList.remove('hidden');
                loadAdminData();
                return;
            }

            // Non-admin users require approval
            const user = users.find(u => u.username === username && u.password === password && u.role === role && u.status === 'approved');

            if (user) {
                localStorage.setItem('currentUser', JSON.stringify(user));
                updateNavBar();
                showSection(`${role}Dashboard`);
                document.getElementById('logoutLink').classList.remove('hidden');

                // Load dashboard data
                if (role === 'producer') {
                    loadProductionHistory();
                } else if (role === 'transporter') {
                    loadShipments();
                } else if (role === 'admin') {
                    loadAdminData();
                }
            } else {
                alert('Invalid credentials or registration not approved');
            }
        }

        function logout() {
            localStorage.removeItem('currentUser');
            updateNavBar();
            showSection('welcome');
            document.getElementById('logoutLink').classList.add('hidden');
        }

        function approveRegistration(username) {
            const users = JSON.parse(localStorage.getItem('users'));
            const user = users.find(u => u.username === username && u.status === 'pending');
            if (user) {
                user.status = 'approved';
                localStorage.setItem('users', JSON.stringify(users));
                loadAdminData();
                alert(`User ${username} approved`);
            }
        }

        function rejectRegistration(username) {
            let users = JSON.parse(localStorage.getItem('users'));
            users = users.filter(u => u.username !== username || u.status !== 'pending');
            localStorage.setItem('users', JSON.stringify(users));
            loadAdminData();
            alert(`User ${username} rejected`);
        }

        function loadAdminData() {
            const users = JSON.parse(localStorage.getItem('users'));
            const productions = JSON.parse(localStorage.getItem('productions'));
            const shipments = JSON.parse(localStorage.getItem('shipments'));
            const orders = JSON.parse(localStorage.getItem('orders'));
            const driverInfo = JSON.parse(localStorage.getItem('driverInfo'));
            const emergencySMS = JSON.parse(localStorage.getItem('emergencySMS'));

            // Pending Registrations
            const registrationTable = document.getElementById('registrationTable');
            registrationTable.innerHTML = '';
            users.filter(u => u.status === 'pending').forEach(user => {
                const row = document.createElement('tr');
                row.innerHTML = `
                    <td class="border p-3">${user.username}</td>
                    <td class="border p-3">${user.role}</td>
                    <td class="border p-3">
                        <button onclick="approveRegistration('${user.username}')" class="bg-teal-600 text-white px-4 py-2 rounded hover:bg-teal-700">Approve</button>
                        <button onclick="rejectRegistration('${user.username}')" class="bg-red-600 text-white px-4 py-2 rounded hover:bg-red-700">Reject</button>
                    </td>
                `;
                registrationTable.appendChild(row);
            });

            // All Users
            const userTable = document.getElementById('userTable');
            userTable.innerHTML = '';
            users.forEach(user => {
                const row = document.createElement('tr');
                row.innerHTML = `
                    <td class="border p-3">${user.username}</td>
                    <td class="border p-3">${user.role}</td>
                    <td class="border p-3">${user.status}</td>
                `;
                userTable.appendChild(row);
            });

            // Productions
            const adminProductionTable = document.getElementById('adminProductionTable');
            adminProductionTable.innerHTML = '';
            productions.forEach(prod => {
                const row = document.createElement('tr');
                row.innerHTML = `
                    <td class="border p-3">${prod.fuelType}</td>
                    <td class="border p-3">${prod.quantity}</td>
                    <td class="border p-3">${prod.date}</td>
                `;
                adminProductionTable.appendChild(row);
            });

            // Shipments
            const adminShipmentTable = document.getElementById('adminShipmentTable');
            adminShipmentTable.innerHTML = '';
            shipments.forEach(ship => {
                const row = document.createElement('tr');
                row.innerHTML = `
                    <td class="border p-3">${ship.fuelType}</td>
                    <td class="border p-3">${ship.quantity}</td>
                    <td class="border p-3">${ship.destination}</td>
                    <td class="border p-3">${ship.status}</td>
                `;
                adminShipmentTable.appendChild(row);
            });

            // Orders
            const adminOrderTable = document.getElementById('adminOrderTable');
            adminOrderTable.innerHTML = '';
            orders.forEach(order => {
                const row = document.createElement('tr');
                row.innerHTML = `
                    <td class="border p-3">${order.fuelType}</td>
                    <td class="border p-3">${order.quantity}</td>
                    <td class="border p-3">${order.location}</td>
                    <td class="border p-3">${order.deliveryDate}</td>
                    <td class="border p-3">${order.status}</td>
                `;
                adminOrderTable.appendChild(row);
            });

            // Driver Info
            const adminDriverTable = document.getElementById('adminDriverTable');
            adminDriverTable.innerHTML = '';
            driverInfo.forEach(driver => {
                const row = document.createElement('tr');
                row.innerHTML = `
                    <td class="border p-3">${driver.lorryType}</td>
                    <td class="border p-3">${driver.experience}</td>
                    <td class="border p-3">${driver.age}</td>
                    <td class="border p-3">${driver.user}</td>
                    <td class="border p-3">${driver.date}</td>
                `;
                adminDriverTable.appendChild(row);
            });

            // Emergency SMS
            const adminEmergencySMSTable = document.getElementById('adminEmergencySMSTable');
            adminEmergencySMSTable.innerHTML = '';
            emergencySMS.forEach(sms => {
                const row = document.createElement('tr');
                row.innerHTML = `
                    <td class="border p-3">${sms.fullName}</td>
                    <td class="border p-3">${sms.telephoneNumber}</td>
                    <td class="border p-3">${sms.location}</td>
                    <td class="border p-3">${sms.fuelType}</td>
                    <td class="border p-3">${sms.fuelAmount}</td>
                    <td class="border p-3">${sms.message}</td>
                    <td class="border p-3">${sms.date}</td>
                `;
                adminEmergencySMSTable.appendChild(row);
            });
        }

        function addProduction() {
            const fuelType = document.getElementById('fuelType').value;
            const quantity = document.getElementById('quantity').value;

            if (!quantity || quantity <= 0) {
                alert('Please enter a valid quantity');
                return;
            }

            const productions = JSON.parse(localStorage.getItem('productions'));
            const newProduction = {
                id: Date.now(),
                fuelType,
                quantity,
                date: new Date().toLocaleString()
            };
            productions.push(newProduction);
            localStorage.setItem('productions', JSON.stringify(productions));

            // Add to shipments for transporters
            const shipments = JSON.parse(localStorage.getItem('shipments'));
            shipments.push({
                ...newProduction,
                destination: 'TBD',
                status: 'Pending'
            });
            localStorage.setItem('shipments', JSON.stringify(shipments));

            loadProductionHistory();
            document.getElementById('quantity').value = '';
        }

        function loadProductionHistory() {
            const productions = JSON.parse(localStorage.getItem('productions'));
            const tbody = document.getElementById('productionTable');
            tbody.innerHTML = '';

            productions.forEach(prod => {
                const row = document.createElement('tr');
                row.innerHTML = `
                    <td class="border p-3">${prod.fuelType}</td>
                    <td class="border p-3">${prod.quantity}</td>
                    <td class="border p-3">${prod.date}</td>
                `;
                tbody.appendChild(row);
            });
        }

        function loadShipments() {
            const shipments = JSON.parse(localStorage.getItem('shipments'));
            const tbody = document.getElementById('shipmentTable');
            tbody.innerHTML = '';

            shipments.forEach(ship => {
                const row = document.createElement('tr');
                row.innerHTML = `
                    <td class="border p-3">${ship.fuelType}</td>
                    <td class="border p-3">${ship.quantity}</td>
                    <td class="border p-3">${ship.destination}</td>
                    <td class="border p-3">
                        <button onclick="updateShipment(${ship.id})" class="bg-teal-600 text-white px-4 py-2 rounded hover:bg-teal-700">Update</button>
                    </td>
                `;
                tbody.appendChild(row);
            });
        }

        function updateShipment(id) {
            const destination = prompt('Enter destination:');
            if (destination) {
                const shipments = JSON.parse(localStorage.getItem('shipments'));
                const shipment = shipments.find(s => s.id === id);
                if (shipment) {
                    shipment.destination = destination;
                    shipment.status = 'In Transit';
                    localStorage.setItem('shipments', JSON.stringify(shipments));
                    loadShipments();
                }
            }
        }

        function findStations() {
            const location = document.getElementById('consumerLocation').value;
            const stationList = document.getElementById('stationList');

            // Mock data for stations
            const stations = [{
                name: 'Shell Station',
                location: 'Nairobi CBD',
                distance: '2km'
            }, {
                name: 'Total Station',
                location: 'Westlands',
                distance: '5km'
            }];

            stationList.innerHTML = '<h4 class="text-lg font-semibold mb-2 text-gray-800">Nearby Stations</h4>';
            stations.forEach(station => {
                stationList.innerHTML += `
                    <p class="text-gray-700">${station.name} - ${station.location} (${station.distance})</p>
                `;
            });
        }

        function orderFuel() {
            const fuelType = document.getElementById('deliveryFuelType').value;
            const quantity = document.getElementById('deliveryQuantity').value;
            const location = document.getElementById('deliveryLocation').value;
            const deliveryDate = document.getElementById('deliveryDate').value;

            if (!quantity || quantity <= 0 || !location || !deliveryDate) {
                alert('Please fill all fields with valid data');
                return;
            }

            const orders = JSON.parse(localStorage.getItem('orders'));
            orders.push({
                id: Date.now(),
                fuelType,
                quantity,
                location,
                deliveryDate,
                status: 'Pending',
                date: new Date().toLocaleString()
            });
            localStorage.setItem('orders', JSON.stringify(orders));

            alert('Order placed successfully!');
            document.getElementById('deliveryQuantity').value = '';
            document.getElementById('deliveryLocation').value = '';
            document.getElementById('deliveryDate').value = '';
        }

        function submitDriverInfo() {
            const lorryType = document.getElementById('lorryType').value;
            const experience = document.getElementById('experience').value;
            const age = document.getElementById('age').value;
            const currentUser = JSON.parse(localStorage.getItem('currentUser'));

            if (!experience || experience < 0 || !age || age < 18) {
                alert('Please fill all fields with valid data');
                return;
            }

            const driverInfo = JSON.parse(localStorage.getItem('driverInfo') || '[]');
            driverInfo.push({
                id: Date.now(),
                lorryType,
                experience,
                age,
                user: currentUser ? currentUser.username : 'Unknown',
                date: new Date().toLocaleString()
            });
            localStorage.setItem('driverInfo', JSON.stringify(driverInfo));

            alert('Driver information submitted successfully!');
            document.getElementById('lorryType').value = 'tanker';
            document.getElementById('experience').value = '';
            document.getElementById('age').value = '';
        }

        function sendEmergencySMS() {
            const fullName = document.getElementById('fullName').value;
            const telephoneNumber = document.getElementById('telephoneNumber').value;
            const location = document.getElementById('emergencyLocation').value;
            const fuelAmount = document.getElementById('fuelAmount').value;
            const fuelType = document.getElementById('fuelType').value;
            const message = document.getElementById('emergencyMessage').value;

            if (!fullName || !telephoneNumber || !location || !fuelAmount || fuelAmount <= 0 || !fuelType || !message) {
                alert('Please fill all fields with valid data');
                return;
            }

            // Store emergency SMS in localStorage
            const emergencySMS = JSON.parse(localStorage.getItem('emergencySMS') || '[]');
            emergencySMS.push({
                id: Date.now(),
                fullName,
                telephoneNumber,
                location,
                fuelAmount,
                fuelType,
                message,
                date: new Date().toLocaleString()
            });
            localStorage.setItem('emergencySMS', JSON.stringify(emergencySMS));

            // Mock SMS sending logic
            const smsContent = `Emergency Request:\nName: ${fullName}\nPhone: ${telephoneNumber}\nLocation: ${location}\nFuel: ${fuelAmount}L ${fuelType}\nMessage: ${message}`;
            alert(`Emergency SMS sent: ${smsContent}`);

            // Clear form
            document.getElementById('fullName').value = '';
            document.getElementById('telephoneNumber').value = '';
            document.getElementById('emergencyLocation').value = '';
            document.getElementById('fuelAmount').value = '';
            document.getElementById('fuelType').value = 'petrol';
            document.getElementById('emergencyMessage').value = '';
        }
    </script>
</body>

</html>
