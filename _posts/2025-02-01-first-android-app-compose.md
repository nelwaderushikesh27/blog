---
layout: post
title: "Building Your First Android App with Jetpack Compose"
date: 2025-02-01
categories: [android, tutorial, jetpack-compose]
tags: [android, jetpack-compose, beginner]
author: Rushikesh
---

# Building Your First Android App with Jetpack Compose

A step-by-step guide for beginners.

## Prerequisites

- Android Studio installed
- Basic Kotlin knowledge
- Android device or emulator

## Step 1: Create a New Project

Open Android Studio → New Project → Empty Compose Activity

## Step 2: Build the UI

```kotlin
@Composable
fun Greeting(name: String, modifier: Modifier = Modifier) {
    Column(
        modifier = modifier.padding(16.dp),
        horizontalAlignment = Alignment.CenterHorizontally
    ) {
        Text(
            text = "Hello, $name!",
            style = MaterialTheme.typography.headlineLarge,
            color = MaterialTheme.colorScheme.primary
        )
        Spacer(modifier = Modifier.height(16.dp))
        Button(onClick = { /* TODO */ }) {
            Text("Click Me")
        }
    }
}
```

## Step 3: Add Interactivity

```kotlin
@Composable
fun CounterApp() {
    var count by remember { mutableStateOf(0) }
    
    Column(
        modifier = Modifier.fillMaxSize(),
        horizontalAlignment = Alignment.CenterHorizontally,
        verticalArrangement = Arrangement.Center
    ) {
        Text("Count: $count", style = MaterialTheme.typography.headlineLarge)
        Button(onClick = { count++ }) {
            Text("Increment")
        }
    }
}
```

## Step 4: Preview Your UI

Compose has built-in previews:

```kotlin
@Preview(showBackground = true)
@Composable
fun DefaultPreview() {
    MyFirstAppTheme {
        CounterApp()
    }
}
```

## What's Next?

- State management
- Navigation
- Networking with Retrofit
- Room database

---

*Happy coding! Check out my other posts for more tutorials.*
