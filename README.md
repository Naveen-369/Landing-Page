# Landing_Page Project - Utilizing TailWindCSS

## Overview
This is a responsive webpage designed to provide information about various services offered by the company. The webpage includes sections for navigation, a hero banner, services, pricing plans, and featured posts. It also features a dark mode toggle for enhanced user experience.

## Technologies Used
- HTML5
- Tailwind CSS for styling
- JavaScript for dark mode toggle functionality
- Google Fonts for typography

## File Structure
```
LandingPage/
├── assets/
│   ├── HeroBanner.png
│   ├── WebDevelopement.png
│   ├── MobileApplication.png
│   ├── Design.png
|   ├── FeaturedPost1.png
|   ├── FeaturedPost2.png
|   ├── FeaturedPost3.png
|   └── FeaturedPost4.png
├── src/
│   ├── index.html
│   ├── input.css
│   └── output.css
|
├──node_modules/...
├── Package.json
└── tailwind.config.js
```

## Detailed Section Breakdown

### Navigation Section
This section provides a navigational menu for the webpage. It includes links to different sections such as Home, Services, Pricing, About, and Contact. It also includes a Sign-Up button and a dark mode toggle.

```html
<section class="container mx-auto mt-2 py-3 px-5 pl-9 border-2 rounded-[30px] Navigation_Enclosure dark:Navigation_Enclosure_Dark">
    <nav class="flex justify-between items-center">
        <ul class="hidden md:flex space-x-10 font-serif font-medium">
            <li><a href="#" class="Navigation_Options dark:Navigation_Options_Dark">Home</a></li>
            <li><a href="#" class="Navigation_Options dark:Navigation_Options_Dark">Services</a></li>
            <li><a href="#" class="Navigation_Options dark:Navigation_Options_Dark">Pricing</a></li>
            <li><a href="#" class="Navigation_Options dark:Navigation_Options_Dark">About</a></li>
            <li><a href="#" class="Navigation_Options dark:Navigation_Options_Dark">Contact</a></li>
            <li><a href="#" id="toggleDarkMode" class="Navigation_Options dark:Navigation_Options_Dark">Dark Mode</a></li>
        </ul>
        <button type="button" class="px-6 py-2 border-[1px] rounded-3xl transition-transform hover:scale-110 duration-500 Navigation_Sign_Button dark:Navigation_Sign_Button_Dark">Sign Up</button>
    </nav>
</section>
```

### Hero Section
The hero section provides an introductory paragraph about learning photo editing. It includes a "Get Started" button and an image.

```html
<section class="flex mt-12 mx-14">
    <section class="p-3 flex flex-1 flex-col text-xl mx-14 justify-center items-center dark:text-white">
        <p>Learning photo editing is a valuable skill...</p>
        <button class="px-4 py-2 bg-red-500 mt-6 transition-transform hover:scale-110 duration-500 rounded-3xl dark:bg-red-800">Get Started</button>
    </section>
    <section class="flex-1">
        <img src="../assets/HeroBanner.png" alt="Dogg">
    </section>
</section>
```

### Services Section
This section showcases the different services offered by the company. Each service is represented by an image and a brief description.

```html
<h2 class="my-12 text-center text-6xl font-serif text-black dark:text-white">Explore our Services</h2>
<section class="flex mx-6 justify-around">
    <article class="Service_Tile">
        <img src="../assets/WebDevelopement.png" alt="Web Developement" class="rounded-tr-3xl rounded-tl-3xl">
        <h3 class="text-3xl text-black p-6 text-center dark:text-white">Web Developement</h3>
        <p class="text-left text-black font-thin text-base dark:text-white">Lorem Ipsum is simply dummy text...</p>
    </article>
    <article class="Service_Tile">
        <img src="../assets/MobileApplication.png" alt="Appilcation developement" class="rounded-tr-3xl rounded-tl-3xl">
        <h3 class="text-3xl text-black p-6 text-center dark:text-white">Mobile Application Developement</h3>
        <p class="text-left text-black font-thin text-base dark:text-white">Lorem Ipsum is simply dummy text...</p>
    </article>
    <article class="Service_Tile">
        <img src="../assets/Design.png" alt="Design" class="rounded-tr-3xl rounded-tl-3xl">
        <h3 class="text-3xl text-black p-6 text-center dark:text-white">Design - UI & UX</h3>
        <p class="text-left text-black font-thin text-base dark:text-white">Lorem Ipsum is simply dummy text...</p>
    </article>
</section>
```

### Pricing Section
The pricing section displays various subscription plans offered by the company. Each plan is highlighted with its features and pricing.

```html
<h1 class="text-red-500 text-center font-serif font-bold text-[42px] mt-6">Pricing</h1>
<h2 class="text-center text-3xl font-semibold font-arsenalSC text-black dark:text-white">Offers multiple packages for Monthly and Yearly Subscriptions</h2>
<h2 class="text-center text-3xl font-semibold font-arsenalSC text-black dark:text-white">Featured plans are here</h2>

<section class="flex justify-evenly mt-12">
    <!-- Basic Plan -->
    <article class="Pricing_Tile shadow-md hover:shadow-3xl hover:shadow-black">
        <h3 class="text-black text-center text-[45px] font-Maname font-medium mb-7 dark:text-white">$99</h3>
        <h3 class="text-red-500 text-center text-[45px] font-Maname font-semibold mb-7">Basic</h3>
        <div class="flex mb-3 items-center text-black dark:text-white">
            <svg xmlns="http://www.w3.org/2000/svg" class="mx-2" height="24px" viewBox="0 -960 960 960" width="24px" fill="red">
                <path d="M200-120q-33 0-56.5-23.5T120-200v-560q0-33 23.5-56.5T200-840h560q8 0 15 1.5t14 4.5l-74 74H200v560h560v-266l80-80v346q0 33-23.5 56.5T760-120H200Zm261-160L235-506l56-56 170 170 367-367 57 55-424 424Z"/>
            </svg>
            Core Business requirement
        </div>
        <!-- Repeat the above block for each feature of the plan -->
    </article>
   
    <!-- Advanced Plan -->
    <article class="Pricing_Tile border-4 border-red-300 dark:border-red-700 border-dashed shadow-md hover:shadow-3xl hover:shadow-black">
        <h3 class="text-black text-center text-[45px] font-Maname font-medium mb-7 dark:text-white">$199</h3>
        <h3 class="text-red-500 text-center text-[45px] font-Maname font-semibold mb-7">Advanced</h3>
        <div class="flex mb-3 items-center text-black dark:text-white">
            <svg xmlns="http://www.w3.org/2000/svg" class="mx-2" height="24px" viewBox="0 -960 960 960" width="24px" fill="red">
                <path d="M200-120q-33 0-56.5-23.5T120-200v-560q0-33 23.5-56.5T200-840h560q8 0 15 1.5t14 4.5l-74 74H200v560h560v-266l80-80v346q0 33-23.5 56.5T760-120H200Zm261-160L235-506l56-56 170 170 367-367 57 55-424 424Z"/>
            </svg>
            Core Business requirement
        </div>
        <!-- Repeat the above block for each feature of the plan -->
    </article>
   
    <!-- Business Plan -->
    <article class="Pricing_Tile shadow-md hover:shadow-3xl hover:shadow-black">
        <h3 class="text-black text-center text-[45px] font-Maname font-medium mb-7 dark:text-white">$299</h3>
        <h3 class="text-red-500 text-center text-[45px] font-Maname font-semibold mb-7">Business</h3>
        <div class="flex mb-3 items-center text-black dark:text-white">
            <svg xmlns="http://www.w3.org/2000/svg"

 class="mx-2" height="24px" viewBox="0 -960 960 960" width="24px" fill="red">
                <path d="M200-120q-33 0-56.5-23.5T120-200v-560q0-33 23.5-56.5T200-840h560q8 0 15 1.5t14 4.5l-74 74H200v560h560v-266l80-80v346q0 33-23.5 56.5T760-120H200Zm261-160L235-506l56-56 170 170 367-367 57 55-424 424Z"/>
            </svg>
            Core Business requirement
        </div>
        <!-- Repeat the above block for each feature of the plan -->
    </article>
</section>
```

### Feature Posts Section
This section displays featured posts related to the company's services. Each post includes an image and a brief description.

```html
<section class="mt-6 mb-4 px-2 py-6 text-center border-b-[1px] border-gray-600">
    <h2 class="text-6xl font-serif dark:text-white">Features Post</h2>
</section>

<section class="flex flex-col lg:flex-row justify-around mt-6">
    <article class="Feature_Tile shadow-xl hover:shadow-3xl hover:shadow-black">
        <img src="../assets/Design.png" alt="Design Image" class="rounded-tl-3xl rounded-tr-3xl">
        <p class="text-black font-bold font-serif text-3xl mt-4 text-center dark:text-white">Lorem Ipsum</p>
        <p class="text-black text-2xl font-arsenal text-left p-3 font-medium dark:text-white">Lorem Ipsum is simply dummy text of the printing and typesetting industry...</p>
    </article>
    <article class="Feature_Tile shadow-xl hover:shadow-3xl hover:shadow-black">
        <img src="../assets/Design.png" alt="Design Image" class="rounded-tl-3xl rounded-tr-3xl">
        <p class="text-black font-bold font-serif text-3xl mt-4 text-center dark:text-white">Lorem Ipsum</p>
        <p class="text-black text-2xl font-arsenal text-left p-3 font-medium dark:text-white">Lorem Ipsum is simply dummy text of the printing and typesetting industry...</p>
    </article>
    <article class="Feature_Tile shadow-xl hover:shadow-3xl hover:shadow-black">
        <img src="../assets/Design.png" alt="Design Image" class="rounded-tl-3xl rounded-tr-3xl">
        <p class="text-black font-bold font-serif text-3xl mt-4 text-center dark:text-white">Lorem Ipsum</p>
        <p class="text-black text-2xl font-arsenal text-left p-3 font-medium dark:text-white">Lorem Ipsum is simply dummy text of the printing and typesetting industry...</p>
    </article>
</section>
```

## Scripts and Styles

### Dark Mode Toggle Script
The JavaScript code for the dark mode toggle switches the theme between light and dark modes based on user interaction and system preferences.

```javascript
const toggleDarkModeButton = document.getElementById('toggleDarkMode');

toggleDarkModeButton.addEventListener('click', function() {
  document.body.classList.toggle('dark');
});
```

### Custom Tailwind CSS Configuration
The custom Tailwind CSS configuration (`output.css`) includes styles tailored to the design of the webpage, ensuring a consistent look and feel across all sections.

```css
/* Custom Tailwind CSS output */
@tailwind base;
@tailwind components;
@tailwind utilities;

.Navigation_Enclosure {
  /* Custom styles */
}

.Navigation_Enclosure_Dark {
  /* Custom dark mode styles */
}

/* Additional custom styles */
```
## Usage
### 1. Clone the Repository
Fork the repository and clone it in your local machine.
```git
git clone "https://github.com/Naveen-369/Landing-Page.git"
cd Landing-Page
```

### 2. Install Dependencies
Install the necessary node modules using the package manager.
```npm
npm install
```
### 3. Open in Browser
Open the project in the browser. Now you can view the project.

## Contribution
To contribute to the project do the above steps and run the following command in the terminal.
```shell
npx tailwindcss -i ./src/input.css -o ./src/output.css --watch
```
Now start developing your changes in the project and create a pull request.

## Conclusion
This webpage is designed to be responsive, user-friendly, and visually appealing. The implementation of dark mode enhances the user experience, providing a modern and accessible interface. The detailed breakdown of each section ensures clarity and ease of maintenance.
