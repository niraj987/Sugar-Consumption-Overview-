<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Global Sugar Consumption Dataset - README</title>
    <!-- Fonts -->
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600;700&display=swap" rel="stylesheet">
    <!-- Tailwind CSS -->
    <script src="https://cdn.tailwindcss.com"></script>
    <!-- Font Awesome -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.2/css/all.min.css">
    <!-- AOS for Animations -->
    <link href="https://unpkg.com/aos@2.3.1/dist/aos.css" rel="stylesheet">
    <style>
        body {
            font-family: 'Poppins', sans-serif;
            line-height: 1.6;
            color: #333;
            margin: 0;
            transition: background-color 0.3s, color 0.3s;
        }
        body.dark-mode {
            background-color: #1a202c;
            color: #e2e8f0;
        }
        .hero {
            background: linear-gradient(rgba(0,0,0,0.5), rgba(0,0,0,0.5)), url('https://images.unsplash.com/photo-1593617403810-3b3b4f2c7d7b?q=80&w=2070&auto=format&fit=crop');
            background-size: cover;
            background-position: center;
            color: white;
            text-align: center;
            padding: 100px 20px;
        }
        .container {
            max-width: 900px;
            margin: 0 auto;
            padding: 20px;
        }
        .section-header {
            cursor: pointer;
            display: flex;
            align-items: center;
            gap: 10px;
        }
        .section-content {
            display: none;
        }
        .section-content.active {
            display: block;
        }
        .back-to-top {
            position: fixed;
            bottom: 20px;
            right: 20px;
            background-color: #3498db;
            color: white;
            padding: 10px;
            border-radius: 50%;
            display: none;
        }
        .hamburger {
            display: none;
        }
        @media (max-width: 768px) {
            .hamburger {
                display: block;
                position: fixed;
                top: 20px;
                right: 20px;
                z-index: 1000;
            }
            .nav-menu {
                display: none;
                position: fixed;
                top: 0;
                left: 0;
                width: 100%;
                background: #2c3e50;
                padding: 20px;
            }
            .nav-menu.active {
                display: block;
            }
        }
    </style>
</head>
<body class="bg-gray-100">
    <!-- Hero Section -->
    <section class="hero" data-aos="fade-down">
        <h1 class="text-5xl font-bold">Global Sugar Consumption Dataset</h1>
        <p class="text-xl mt-4">Uncover Sweet Insights from 1960 to 2023</p>
        <a href="#overview" class="mt-6 inline-block bg-blue-500 text-white py-2 px-6 rounded-lg hover:bg-blue-600">Explore Now</a>
    </section>

    <!-- Navigation -->
    <nav class="bg-gray-800 text-white p-4 sticky top-0 z-50">
        <div class="container flex justify-between items-center">
            <div class="hamburger md:hidden">
                <i class="fas fa-bars text-2xl cursor-pointer"></i>
            </div>
            <ul class="nav-menu flex space-x-6 md:flex md:items-center">
                <li><a href="#overview" class="hover:text-blue-400">Overview</a></li>
                <li><a href="#dataset" class="hover:text-blue-400">Dataset</a></li>
                <li><a href="#usage" class="hover:text-blue-400">Usage</a></li>
                <li><a href="#visualizations" class="hover:text-blue-400">Visualizations</a></li>
                <li><a href="#faq" class="hover:text-blue-400">FAQ</a></li>
                <li><button id="theme-toggle" class="text-yellow-400"><i class="fas fa-moon"></i></button></li>
            </ul>
        </div>
    </nav>

    <div class="container">
        <!-- Quick Stats -->
        <section id="stats" class="my-8" data-aos="fade-up">
            <h2 class="text-2xl font-semibold text-gray-800">Quick Stats</h2>
            <div class="grid grid-cols-1 md:grid-cols-3 gap-4 mt-4">
                <div class="bg-blue-100 p-4 rounded-lg text-center">
                    <i class="fas fa-globe text-3xl text-blue-500"></i>
                    <p class="text-xl font-bold">200+ Countries</p>
                    <p>Covered in the dataset</p>
                </div>
                <div class="bg-green-100 p-4 rounded-lg text-center">
                    <i class="fas fa-calendar-alt text-3xl text-green-500"></i>
                    <p class="text-xl font-bold">1960–2023</p>
                    <p>64 years of data</p>
                </div>
                <div class="bg-yellow-100 p-4 rounded-lg text-center">
                    <i class="fas fa-chart-bar text-3xl text-yellow-500"></i>
                    <p class="text-xl font-bold">22 Columns</p>
                    <p>Rich metrics for analysis</p>
                </div>
            </div>
        </section>

        <!-- Overview -->
        <section id="overview" class="my-8" data-aos="fade-up">
            <h2 class="section-header text-2xl font-semibold text-gray-800"><i class="fas fa-info-circle"></i> Overview</h2>
            <div class="section-content bg-white p-6 rounded-lg shadow-lg">
                <p>
                    Dive into the <strong>Global Sugar Consumption Dataset</strong>, a comprehensive resource capturing sugar consumption trends across the globe from 1960 to 2023. Designed for researchers, data enthusiasts, and policymakers, this dataset unlocks insights into dietary patterns, health outcomes, and economic factors.
                </p>
            </div>
        </section>

        <!-- Dataset Description -->
        <section id="dataset" class="my-8" data-aos="fade-up">
            <h2 class="section-header text-2xl font-semibold text-gray-800"><i class="fas fa-database"></i> Dataset Description</h2>
            <div class="section-content bg-white p-6 rounded-lg shadow-lg">
                <p>Available in <code>Sugar_consumption.xlsx</code>, the dataset includes:</p>
                <ul class="list-disc pl-6">
                    <li><strong>Country</strong>: Country name</li>
                    <li><strong>Year</strong>: 1960–2023</li>
                    <li><strong>Country_Code</strong>: ISO code</li>
                    <li><strong>Continent</strong>: Geographical continent</li>
                    <li><strong>Region</strong>: Sub-region</li>
                    <li><strong>Population</strong>: Country population</li>
                    <li><strong>GDP_Per_Capita</strong>: GDP per capita (USD)</li>
                    <li><strong>Per_Capita_Sugar_Consumption</strong>: Sugar per person (kg/year)</li>
                    <li><strong>Total_Sugar_Consumption</strong>: Total sugar (kg)</li>
                    <li><strong>Sugar_From_Sugarcane</strong>: % from sugarcane</li>
                    <li><strong>Sugar_From_Beet</strong>: % from sugar beet</li>
                    <li><strong>Sugar_From_HFCS</strong>: % from HFCS</li>
                    <li><strong>Sugar_From_Other</strong>: % from other sources</li>
                    <li><strong>Processed_Food_Consumption</strong>: Processed food (kg/person/year)</li>
                    <li><strong>Avg_Daily_Sugar_Intake</strong>: Daily sugar (g)</li>
                    <li><strong>Diabetes_Prevalence</strong>: Diabetes rate (%)</li>
                    <li><strong>Obesity_Rate</strong>: Obesity rate (%)</li>
                    <li><strong>Sugar_Imports</strong>: Sugar imports (kg)</li>
                    <li><strong>Sugar_Exports</strong>: Sugar exports (kg)</li>
                    <li><strong>Avg_Retail_Price_Per_Kg</strong>: Sugar price (USD/kg)</li>
                    <li><strong>Urbanization_Rate</strong>: Urban population (%)</li>
                    <li><strong>Sugarcane_Production_Yield</strong>: Yield (tonnes/hectare)</li>
                </ul>
            </div>
        </section>

        <!-- Interactive Chart -->
        <section id="chart" class="my-8" data-aos="fade-up">
            <h2 class="text-2xl font-semibold text-gray-800"><i class="fas fa-chart-pie"></i> Sample Visualization</h2>
            <p class="mb-4">Preview the distribution of sugar sources:</p>
            <div id="sugar-chart" class="bg-white p-4 rounded-lg shadow-lg"></div>
        </section>

        <!-- Usage -->
        <section id="usage" class="my-8" data-aos="fade-up">
            <h2 class="section-header text-2xl font-semibold text-gray-800"><i class="fas fa-rocket"></i> Usage</h2>
            <div class="section-content bg-white p-6 rounded-lg shadow-lg">
                <p>Ideal for:</p>
                <ul class="list-disc pl-6">
                    <li>Tracking sugar consumption trends</li>
                    <li>Correlating sugar intake with health outcomes</li>
                    <li>Analyzing urbanization’s impact on diets</li>
                    <li>Exploring sugar trade and production</li>
                </ul>
            </div>
        </section>

        <!-- Example Visualizations -->
        <section id="visualizations" class="my-8" data-aos="fade-up">
            <h2 class="section-header text-2xl font-semibold text-gray-800"><i class="fas fa-eye"></i> Example Visualizations</h2>
            <div class="section-content bg-white p-6 rounded-lg shadow-lg">
                <ul class="list-disc pl-6">
                    <li>Time-series of sugar consumption</li>
                    <li>Scatter plots of sugar vs. health metrics</li>
                    <li>Bar charts of sugar sources</li>
                    <li>Heatmaps of consumption by continent</li>
                    <li>Import/export trends</li>
                </ul>
            </div>
        </section>

        <!-- Getting Started -->
        <section id="getting-started" class="my-8" data-aos="fade-up">
            <h2 class="section-header text-2xl font-semibold text-gray-800"><i class="fas fa-play"></i> Getting Started</h2>
            <div class="section-content bg-white p-6 rounded-lg shadow-lg">
                <ol class="list-decimal pl-6">
                    <li>Clone: <code>git clone https://github.com/niraj987/Sugar-Consumption-Analysis</code></li>
                    <li>Install: <code>pip install pandas matplotlib seaborn plotly</code></li>
                    <li>Load:
                        <pre class="bg-gray-900 text-gray-300 p-4 rounded-lg">import pandas as pd
df = pd.read_excel("Sugar_consumption.xlsx")</pre>
                    </li>
                </ol>
            </div>
        </section>

        <!-- Example Analysis -->
        <section id="example" class="my-8" data-aos="fade-up">
            <h2 class="section-header text-2xl font-semibold text-gray-800"><i class="fas fa-code"></i> Example Analysis</h2>
            <div class="section-content bg-white p-6 rounded-lg shadow-lg">
                <p>Visualize France’s sugar consumption:</p>
                <pre class="bg-gray-900 text-gray-300 p-4 rounded-lg">import pandas as pd
import matplotlib.pyplot as plt

df = pd.read_excel("Sugar_consumption.xlsx")
france_data = df[df["Country"] == "France"]

plt.figure(figsize=(10, 6))
plt.plot(france_data["Year"], france_data["Per_Capita_Sugar_Consumption"], marker="o")
plt.title("Per Capita Sugar Consumption in France (1960–2023)")
plt.xlabel("Year")
plt.ylabel("Sugar Consumption (kg/person/year)")
plt.grid(True)
plt.savefig("france_sugar.png")
plt.close()</pre>
            </div>
        </section>

        <!-- FAQ -->
        <section id="faq" class="my-8" data-aos="fade-up">
            <h2 class="section-header text-2xl font-semibold text-gray-800"><i class="fas fa-question-circle"></i> FAQ</h2>
            <div class="section-content bg-white p-6 rounded-lg shadow-lg">
                <p><strong>How do I handle negative values?</strong></p>
                <p>Clip negatives to zero: <code>df = df.clip(lower=0)</code>.</p>
                <p><strong>Is the data real?</strong></p>
                <p>It’s synthetic but reflects realistic trends.</p>
                <p><strong>Can I contribute?</strong></p>
                <p>Yes! Submit a PR on <a href="https://github.com/niraj987/Sugar-Consumption-Analysis">GitHub</a>.</p>
            </div>
        </section>

        <!-- Notes -->
        <section id="notes" class="my-8" data-aos="fade-up">
            <h2 class="section-header text-2xl font-semibold text-gray-800"><i class="fas fa-exclamation-circle"></i> Notes</h2>
            <div class="section-content bg-blue-50 p-6 rounded-lg shadow-lg">
                <ul class="list-disc pl-6">
                    <li>Clean negative values in <code>Sugar_From_Other</code>.</li>
                    <li>Data may be incomplete for some years.</li>
                    <li>Validate outliers before analysis.</li>
                </ul>
            </div>
        </section>

        <!-- License -->
        <section id="license" class="my-8" data-aos="fade-up">
            <h2 class="section-header text-2xl font-semibold text-gray-800"><i class="fas fa-balance-scale"></i> License</h2>
            <div class="section-content bg-white p-6 rounded-lg shadow-lg">
                <p>Licensed under the <a href="https://github.com/niraj987/Sugar-Consumption-Analysis/blob/main/LICENSE">MIT License</a>.</p>
            </div>
        </section>

        <!-- Contact -->
        <section id="contact" class="my-8" data-aos="fade-up">
            <h2 class="section-header text-2xl font-semibold text-gray-800"><i class="fas fa-envelope"></i> Contact</h2>
            <div class="section-content bg-white p-6 rounded-lg shadow-lg">
                <p>Open an <a href="https://github.com/niraj987/Sugar-Consumption-Analysis/issues">issue</a> or email <a href="mailto:Kumarniraj11045@gmail.com">Kumarniraj11045@gmail.com</a>.</p>
            </div>
        </section>

        <!-- Contribute CTA -->
        <section class="my-8 text-center" data-aos="zoom-in">
            <h2 class="text-2xl font-semibold text-gray-800">Join the Community</h2>
            <p class="mt-2">Contribute to the dataset or share your visualizations!</p>
            <a href="https://github.com/niraj987/Sugar-Consumption-Analysis" class="mt-4 inline-block bg-green-500 text-white py-2 px-6 rounded-lg hover:bg-green-600">Contribute Now</a>
        </section>
    </div>

    <!-- Footer -->
    <footer class="bg-gray-800 text-white text-center py-6">
        <p>© 2025 Global Sugar Consumption Dataset | Built for Data Enthusiasts | <a href="https://-sm-2xl">View on GitHub</a></p>
    </footer>

    <!-- Back to Top -->
    <a href="#" class="back-to-top"><i class="fas fa-arrow-up"></i></a>

    <!-- Scripts -->
    <script src="https://cdn.jsdelivr.net/npm/plotly@2.27.0/dist/plotly.min.js"></script>
    <script src="https://unpkg.com/aos@2.3.1/dist/aos.js"></script>
    <script>
        // Initialize AOS
        AOS.init();

        // Collapsible Sections
        document.querySelectorAll('.section-header').forEach(header => {
            header.addEventListener('click', () => {
                const content = header.nextElementSibling;
                content.classList.toggle('active');
            });
        });

        // Hamburger Menu
        document.querySelector('.hamburger').addEventListener('click', () => {
            document.querySelector('.nav-menu').classList.toggle('active');
        });

        // Back to Top
        const backToTop = document.querySelector('.back-to-top');
        window.addEventListener('scroll', () => {
            backToTop.style.display = window.scrollY > 300 ? 'block' : 'none';
        });

        // Dark Mode Toggle
        document.getElementById('theme-toggle').addEventListener('click', () => {
            document.body.classList.toggle('dark-mode');
            document.querySelectorAll('.bg-white').forEach(el => el.classList.toggle('bg-gray-800'));
            document.querySelectorAll('.bg-blue-50').forEach(el => el.classList.toggle('bg-gray-700'));
        });

        // Plotly Chart
        const data = [{
            values: [60, 25, 10, 5],
            labels: ['Sugarcane', 'Beet', 'HFCS', 'Other'],
            type: 'pie',
            marker: { colors: ['#ff9999', '#66b3ff', '#99ff99', '#ffcc99'] }
        }];
        const layout = {
            title: 'Sugar Source Distribution',
            height: 400,
            showlegend: true
        };
        Plotly.newPlot('sugar-chart', data, layout);
    </script>
</body>
</html>
