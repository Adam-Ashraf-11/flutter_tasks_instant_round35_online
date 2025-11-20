# Task 4: Math Quiz Game

Create a Dart program that implements an interactive math quiz with multiple difficulty levels and game modes.

## Basic Requirements:

### Main Features:
1. **Number Generation**: The program generates two random numbers between 1 and 10 for each question
2. **User Input**: The program displays the numbers to the user and asks for their multiplication result
3. **Answer Validation**: The program compares user input with the correct answer and provides feedback
4. **Continue Option**: After each answer, the program asks "Do you want to continue? (yes/no)"
5. **Score Tracking**: If user chooses "no", the program displays:
   - Number of correct answers
   - Number of incorrect answers

### Basic Mode Flow:
```
Question 1:
5 × 7 = ? 
Your answer: 35
"Correct answer!"

Do you want to continue? (yes/no): yes

Question 2:
8 × 3 = ? 
Your answer: 25
"Incorrect answer! The correct answer is: 24"

Do you want to continue? (yes/no): no

--- Results ---
Correct answers: 1
Incorrect answers: 1
```

## Advanced Features (Optional):

### 1. Difficulty Levels:
- Allow user to choose difficulty level at the start
- User progresses to higher levels after every three correct answers
- Each new level increases number complexity (e.g., larger numbers, different operations)

### 2. Enhanced Gameplay:
- **Timer**: Add time limits for answers
- **Multiple Operations**: Include addition, subtraction, and division
- **Custom Ranges**: Allow user to set number ranges
- **Progress Tracking**: Show progress bar and level advancement

### 3. Operation Variety:
Allow changing the mathematical operation type:
- Multiplication (default)
- Addition
- Subtraction  
- Division

## Implementation Requirements:

### Core Structure:
```dart
import 'dart:io';
import 'dart:math';

void main() {
  // Initialize variables
  int correctAnswers = 0;
  int incorrectAnswers = 0;
  bool continueGame = true;
  int level = 1;
  int correctInRow = 0;
  
  // Main game loop
  while (continueGame) {
    // Generate numbers based on level
    // Display question
    // Get user input
    // Validate answer
    // Update scores
    // Ask to continue
    // Check for level advancement
  }
  
  // Display final results
}
```

### Sample Advanced Implementation:
```dart
// Example of level-based number generation
int generateNumber(int level) {
  Random random = Random();
  switch (level) {
    case 1:
      return random.nextInt(10) + 1; // 1-10
    case 2:
      return random.nextInt(50) + 1; // 1-50
    case 3:
      return random.nextInt(100) + 1; // 1-100
    default:
      return random.nextInt(100) + 1;
  }
}

// Example of operation selection
String getOperationSymbol(String operationType) {
  switch (operationType) {
    case 'addition':
      return '+';
    case 'subtraction':
      return '-';
    case 'multiplication':
      return '×';
    case 'division':
      return '÷';
    default:
      return '×';
  }
}
```

## Expected Output Examples:

### Basic Mode:
```
🎯 Welcome to Math Quiz! 🎯

Question 1:
4 × 6 = ? 
Your answer: 24
"Correct answer!"

Continue? (yes/no): yes

Question 2:
9 × 7 = ? 
Your answer: 56
"Incorrect answer! The correct answer is: 63"

Continue? (yes/no): no

📊 Final Results:
✅ Correct: 1
❌ Incorrect: 1
```

### Advanced Mode with Levels:
```
Choose difficulty level (1-3): 1

Level 1 - Question 1:
3 × 8 = ? 
Your answer: 24
✅ Correct! 

Level 1 - Question 2:
5 × 7 = ? 
Your answer: 35
✅ Correct!

Level 1 - Question 3:
9 × 2 = ? 
Your answer: 18
✅ Correct!

🎉 Level Up! Now starting Level 2...

Level 2 - Question 1:
12 × 15 = ? 
...
```

## Bonus Features:
- Add sound effects for correct/incorrect answers
- Implement a high score system
- Add visual progress indicators
- Include multiple game modes (timed, survival, etc.)
- Export results to a file

This task combines basic input/output operations with game logic, conditionals, loops, and optional advanced features for a comprehensive Dart programming exercise.