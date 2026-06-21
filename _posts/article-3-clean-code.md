---
layout: default
title: Article - Clean Code in JavaScript
---

# Clean Code Principles in JavaScript

**Published:** January 2026 | **Reading time:** 6 min

---

## Introduction

Writing clean code isn't just about making it work—it's about making it maintainable, understandable, and elegant. These principles are especially important in JavaScript.

## Why Clean Code Matters

Clean code is:
- **Easier to maintain**: Future you (and others) will thank you
- **Less prone to bugs**: Clarity reveals logical errors
- **Faster to develop**: Less time spent debugging
- **More professional**: Shows competence and care

## Naming Conventions

### Use Meaningful Names

**Bad:**
```javascript
const d = new Date();
const x = user.age;
```

**Good:**
```javascript
const currentDate = new Date();
const userAge = user.age;
```

### Functions Should Describe Intent

**Bad:**
```javascript
function proc(arr) {
  return arr.filter(x => x > 10);
}
```

**Good:**
```javascript
function filterNumbersGreaterThanTen(numbers) {
  return numbers.filter(num => num > 10);
}
```

## Keep Functions Small and Focused

### Single Responsibility Principle

**Bad:**
```javascript
function processUser(user) {
  // Validation
  if (!user.email) throw new Error('Invalid email');
  
  // API call
  const response = fetch('/api/users', { method: 'POST', body: user });
  
  // Send email
  sendEmail(user.email);
  
  // Log
  console.log('User created');
}
```

**Good:**
```javascript
function validateUser(user) {
  if (!user.email) throw new Error('Invalid email');
}

function createUser(user) {
  return fetch('/api/users', { method: 'POST', body: user });
}

async function processUserRegistration(user) {
  validateUser(user);
  await createUser(user);
  await sendEmail(user.email);
  logUserCreation(user);
}
```

## Avoid Magic Numbers

**Bad:**
```javascript
if (user.age > 18 && user.subscription === 2) {
  // Do something
}
```

**Good:**
```javascript
const LEGAL_AGE = 18;
const PREMIUM_SUBSCRIPTION = 2;

if (user.age > LEGAL_AGE && user.subscription === PREMIUM_SUBSCRIPTION) {
  // Do something
}
```

## Comments: Show Intent, Not Implementation

**Bad:**
```javascript
// Check if age is greater than 18
if (age > 18) { }
```

**Good:**
```javascript
// Allow access only to adults
if (age > LEGAL_AGE) { }
```

## Error Handling

**Bad:**
```javascript
try {
  getData();
} catch (e) {
  // Silently fail
}
```

**Good:**
```javascript
try {
  getData();
} catch (error) {
  logger.error('Failed to fetch data:', error);
  throw new UserFacingError('Data loading failed');
}
```

## Use Destructuring

**Bad:**
```javascript
const name = user.profile.name;
const email = user.profile.email;
```

**Good:**
```javascript
const { name, email } = user.profile;
```

## Avoid Deep Nesting

**Bad:**
```javascript
if (user) {
  if (user.active) {
    if (user.roles.includes('admin')) {
      doSomething();
    }
  }
}
```

**Good:**
```javascript
if (!user || !user.active || !user.roles.includes('admin')) return;
doSomething();
```

## DRY - Don't Repeat Yourself

**Bad:**
```javascript
const totalA = items.reduce((sum, item) => sum + item.price, 0);
const totalB = products.reduce((sum, product) => sum + product.price, 0);
```

**Good:**
```javascript
function calculateTotal(items) {
  return items.reduce((sum, item) => sum + item.price, 0);
}

const totalA = calculateTotal(items);
const totalB = calculateTotal(products);
```

## Conclusion

Clean code is an ongoing practice. Start with these principles and continuously refine your coding style. Your future self will appreciate the effort!

---

[← Back to Articles](./articles.html)
