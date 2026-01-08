# Inuit Shoes Chatbot – Analyst Intern Assignment (Task 1)

## Objective
The goal of this chatbot is to reduce user drop-offs on the Inuit website by:
- Guiding users through product discovery
- Educating them about shoe quality
- Encouraging home delivery orders
The conversation is designed to be short, simple, and personal.

## Chatbot Personality & Tone
- Friendly and premium
- Conversational and helpful
- Easy navigation using buttons
- Minimal typing required from users

## Chatbot Conversation Flow

### 1. Welcome & Brand Introduction
The bot greets users and introduces Inuit as a premium footwear brand.

**User Options:**
- Explore Shoes
- About Inuit
- Exit

---

### 2. Shoe Preference Collection
The bot asks users about:
- Shoe type (Formal, Casual, Sneakers)
- Shoe size (via quick replies)

This helps personalize the experience.

---

### 3. Product Education
The bot shows short videos explaining:
- Premium leather selection
- Handcrafted manufacturing
- Quality and comfort testing

---

### 4. Order Placement
Users are asked if they want home delivery.
The bot collects:
- Delivery address
- Contact number
- Payment method (Card / UPI / COD)

---

### 5. Fallback Handling
If the bot does not understand user input, it responds politely and redirects users using buttons such as:
- Explore Shoes
- Track Order
- Contact Support

flowchart TD
    A[User visits Inuit Website] --> B[Welcome Message & Brand Intro]
    B --> C{What does user want to do?}

    C -->|Explore Shoes| D[Ask Shoe Type]
    C -->|About Inuit| E[Show Brand Info]
    C -->|Exit| Z[End Chat]

    D --> F[Ask Shoe Size]
    F --> G[Show How Inuit Shoes Are Made<br/>(Video Carousel)]

    G --> H{Interested in buying?}
    H -->|Yes| I[Ask for Home Delivery]
    H -->|Explore More| D

    I --> J[Collect Address & Payment Method]
    J --> K[Order Confirmed]
    K --> Z[Thank You & Exit]

    %% Fallback
    B --> X[User Enters Unknown Message]
    D --> X
    G --> X
    X --> Y[Fallback Message with Buttons]
    Y --> C


## Conclusion
This chatbot flow focuses on clarity, personalization, and guided navigation to improve customer engagement and conversion.
