# Yummly-Style Recipe and Meal Planning API

## Overview

This comprehensive recipe API provides a rich set of endpoints for culinary enthusiasts, home cooks, and food lovers. The API offers robust functionality for searching recipes, retrieving meal plans, exploring ingredients, and accessing recipe reviews.

This API is listed on [Rapidapi](https://rapidapi.com/belchiorarkad-FqvHs2EDOtP/api/yummly-api1): https://rapidapi.com/belchiorarkad-FqvHs2EDOtP/api/yummly-api1 

## API Endpoints

### 1. Search Endpoints

#### `/search/suggestions`
- **Description**: Provides search suggestions based on user input
- **Parameters**:
  - `query` (required): Search term for recipe suggestions

#### `/search`
- **Description**: Performs a comprehensive recipe search
- **Parameters**:
  - `query` (required): Search term
  - `page` (optional, default: '1'): Page number for pagination
  - `limit` (optional, default: '25'): Number of results per page

### 2. Recipe Endpoints

#### `/recipe/byid`
- **Description**: Retrieves detailed information about a specific recipe
- **Parameters**:
  - `recipeId` (required): Unique identifier for a recipe

#### `/recipe/review/byglobalID`
- **Description**: Fetches reviews for a recipe using a global identifier
- **Parameters**:
  - `globalID` (required): Global recipe identifier
  - `page` (optional, default: '1'): Page of reviews
  - `limit` (optional, default: '4'): Number of reviews per page

#### `/recipe/review/byrecipeID`
- **Description**: Retrieves reviews for a specific recipe
- **Parameters**:
  - `recipeId` (required): Recipe's unique identifier
  - `limit` (optional, default: '4'): Number of reviews to return

#### `/recipe/guided`
- **Description**: Gets a list of guided recipes
- **Parameters**:
  - `page` (optional, default: '1'): Page number
  - `limit` (optional, default: '36'): Number of recipes per page

### 3. Meal Planning Endpoints

#### `/mealplaner`
- **Description**: Retrieves a list of meal plans
- **Parameters**:
  - `include` (optional, default: '5'): Number of meal plans to include

#### `/mealplaner/byId`
- **Description**: Gets details for a specific meal plan
- **Parameters**:
  - `mpId` (optional, default: 'keto'): Meal plan identifier
  - `include` (optional, default: '5'): Number of details to include

### 4. Cuisine and Ingredient Endpoints

#### `/cuisines`
- **Description**: Lists available cuisines
- **Parameters**:
  - `limit` (optional, default: '36'): Number of cuisines to return

#### `/ingredient/byID`
- **Description**: Retrieves information about a specific ingredient
- **Parameters**:
  - `ingredientId` (required): Ingredient identifier

#### `/ingredient`
- **Description**: Returns a list of all ingredients

### 5. Blog/Posts Endpoint

#### `/posts`
- **Description**: Searches and retrieves blog posts or articles
- **Parameters**:
  - `query` (required): Search term
  - `page` (optional, default: '1'): Page number
  - `limit` (optional, default: '10'): Number of posts per page

## Error Handling

The API consistently returns JSON responses with the following structure:
- `status`: Indicates the result ('success', 'error', 'missing_argument')
- `message`: Provides detailed information about the response
- `data`: Contains the actual response payload

### Example Error Response
```json
{
  "status": "missing_argument",
  "message": "Please provide the query",
  "data": null
}
```

## Recommended Usage on RapidAPI

1. **Authentication**: Ensure you have the correct API key from RapidAPI
2. **Rate Limits**: Be mindful of your subscription's request limits
3. **Pagination**: Utilize page and limit parameters for efficient data retrieval

## Sample API Call (using fetch)

```javascript
const options = {
  method: 'GET',
  headers: {
    'X-RapidAPI-Key': 'YOUR_RAPIDAPI_KEY',
    'X-RapidAPI-Host': 'yummly-api1.p.rapidapi.com'
  }
};

// Search for recipes
fetch('https://yummly-api1.p.rapidapi.com/search?query=pasta&page=1&limit=10', options)
  .then(response =&gt; response.json())
  .then(data =&gt; console.log(data))
  .catch(error =&gt; console.error('Error:', error));
```

## Potential Use Cases

- Recipe discovery applications
- Meal planning services
- Cooking and nutrition tracking apps
- Food blogs and content platforms

Here's a complete piece of content about **Yummly**, including an overview and frequently asked questions (FAQs):

---

## **What is Yummly?**

Yummly is a comprehensive recipe discovery and meal planning platform designed to simplify cooking for people of all skill levels. It provides personalized recipes, grocery lists, and meal recommendations based on user preferences, dietary restrictions, and cooking goals.

Founded in 2009 and later acquired by Whirlpool Corporation, **Yummly** uses advanced filtering, artificial intelligence, and visual tools to make meal planning and cooking seamless. The platform is available as a website and a mobile app (iOS and Android), offering free and premium features to enhance the cooking experience.

### **Key Features of Yummly:**
1. **Personalized Recipes:**  
   Yummly curates recipe recommendations tailored to your tastes, dietary needs (e.g., gluten-free, vegan, keto), and allergies.

2. **Advanced Search Filters:**  
   Users can filter recipes based on ingredients, cooking time, cuisine, nutrition facts, and difficulty level.

3. **Smart Grocery List:**  
   Yummly helps create a grocery shopping list directly from recipes, allowing users to check off ingredients as they shop.

4. **Step-by-Step Guided Recipes:**  
   Many recipes come with video guides and voice prompts for step-by-step cooking instructions.

5. **Integration with Smart Devices:**  
   The app connects with Whirlpool smart appliances to enable smart cooking.

6. **Yummly Pro (Premium):**  
   Yummly Pro provides exclusive video lessons from professional chefs, additional recipes, and meal planning tools.

7. **Meal Planner:**  
   The platform lets users plan meals for the week, track calories, and streamline grocery shopping.

---

## **FAQs About Yummly**

### **1. Is Yummly free to use?**  
Yes, Yummly offers a free version that includes access to thousands of recipes, advanced filters, and a grocery list feature. However, there is also a premium version called Yummly Pro, which provides exclusive content and video lessons.

---

### **2. What is Yummly Pro, and is it worth it?**  
Yummly Pro is a subscription-based service that provides premium features like step-by-step video tutorials from professional chefs, exclusive recipes, and enhanced meal-planning tools. It’s ideal for individuals looking to expand their cooking skills and try new recipes.

---

### **3. Can I filter recipes for specific dietary restrictions?**  
Absolutely! Yummly allows users to filter recipes based on dietary needs such as gluten-free, vegetarian, vegan, keto, dairy-free, nut-free, and more.

---

### **4. How does Yummly's grocery list feature work?**  
When you save a recipe, Yummly automatically adds its ingredients to a grocery list. You can check off items as you shop, making it a convenient tool for meal prep.

---

### **5. Can I connect Yummly with smart kitchen devices?**  
Yes, Yummly integrates seamlessly with Whirlpool smart appliances, allowing you to send cooking instructions directly to compatible ovens and other devices.

---

### **6. Is Yummly available on mobile?**  
Yes, Yummly has a user-friendly app available for both iOS and Android devices. You can sync your account across multiple devices to access your recipes and grocery lists anytime.

---

### **7. How do I save recipes on Yummly?**  
You can save recipes by creating a free Yummly account. Simply click the “Save” button on any recipe, and it will be added to your digital recipe box for future use.

---

### **8. Does Yummly support meal planning?**  
Yes, Yummly’s meal planner allows you to schedule meals for the week, ensuring a variety of dishes while meeting your dietary and calorie goals.

---

### **9. What types of cuisines are available on Yummly?**  
Yummly provides recipes from a wide range of cuisines, including American, Italian, Mexican, Asian, Mediterranean, and many more.

---

### **10. How does Yummly personalize recipe recommendations?**  
Yummly uses AI and user input, such as taste preferences, allergens, disliked ingredients, and previous searches, to recommend recipes tailored to your needs.

---

### **11. Can I use Yummly offline?**  
While the core features require internet access, you can save recipes and refer to them later when offline.

---

### **12. How can I subscribe to Yummly Pro?**  
You can subscribe to Yummly Pro directly through the Yummly app or website. The service typically offers a free trial before switching to a paid subscription.

---

## **Conclusion**

Yummly is the ultimate kitchen assistant for anyone looking to explore new recipes, simplify meal prep, or take their cooking to the next level. Whether you’re a beginner or an experienced cook, Yummly’s smart tools and personalized recommendations help you enjoy hassle-free cooking every day.

---
