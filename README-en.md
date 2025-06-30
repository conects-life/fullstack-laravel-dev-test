# 🧪 Technical Test – Full Stack Laravel Developer

## 🎯 Test Objective

Evaluate the candidate’s skills in the following technical areas:

- **Languages:** PHP PHP ([Laravel](https://laravel.com/), [Filament](https://filamentphp.com/)), MySQL, JavaScript ([AlpineJS](https://alpinejs.dev/), [Livewire](https://livewire.laravel.com/)), HTML, CSS ([TailwindCSS](https://tailwindcss.com/))  
- **Concepts:** Use of queues and asynchronous tasks, ability to read and understand technical documentation  
- **Frameworks/Tooling:** Laravel, Filament, Livewire, AlpineJS, TailwindCSS  
- **Database:** Modeling with Eloquent, **with special attention to managing relationships between models**

---

## 🌐 Data Source to Use

The data source from which to extract the information for import is:

🔗 [https://sandbox.oxylabs.io/products](https://sandbox.oxylabs.io/products)

The crawler script should extract data such as:

- `title`  
- `price`  
- `image_url`  
- `description` (if available)  
- `category` or another useful field for classification

---

## 🧪 Test Structure

### ✅ 1. Create a PHP Crawler

- Write a PHP script to scrape data from the website above.  
- The crawler must export the data in JSON format readable by Laravel.  
- You may use any library (cURL, Guzzle, Symfony DomCrawler, etc.).

### ✅ 2. Laravel Backend – Asynchronous Import

- Create a new Laravel project.  
- Create two Eloquent models:  
  - `Product`: representing the product  
  - `Image`: representing one or more associated images  
- Make sure to **properly manage the relationships between models**.  
- Create a `POST /api/import` route to receive JSON data from the crawler.  
- The import must be done **asynchronously**, using a **queue system** with a dedicated **Job**.

### ✅ 3. Filament Admin Panel

- Install Filament in the project.  
- Create a Filament **Resource** (`ProductResource`) to:  
  - View all products  
  - Edit or delete records  
  - Display a preview image in the product list

### ✅ 4. Dynamic Frontend – Livewire + AlpineJS

- Create a page accessible at `/view/products`.  
- The page must:  
  - Display paginated products (25 per page, at least 2 pages)  
  - Allow sorting by date added or other criteria  
  - Be dynamic using **Livewire + AlpineJS**  
  - Have a clean and responsive style using **TailwindCSS**

---

## 📝 Evaluation Criteria

| Area                     | Evaluation Focus                                             |
|--------------------------|--------------------------------------------------------------|
| **PHP**                  | Code cleanliness, structure, use of scraping libraries       |
| **Laravel**              | Best practices, asynchronous handling, API design            |
| **Eloquent**             | Modeling, relationships between models                        |
| **Filament**             | Integration and effective use of the admin panel              |
| **Livewire/AlpineJS**    | Frontend reactivity without page reload                       |
| **TailwindCSS**          | Consistent use of utilities, responsive design                |
| **Soft Skills**          | Clarity, organization, documentation skills                   |

---

## ⏱️ Estimated Time

**6–12 hours.** The test can be completed in multiple stages. Partial submissions are allowed if well documented.

---

## 📦 Submission

- Link to the repository (GitHub, GitLab, Bitbucket)  
- Complete README with installation instructions  
- (Optional) Use of Docker, DDEV, or Laravel Sail for quick setup
