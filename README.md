# ZanTest 🇰🇿

**ZanTest** is a modern, high-performance Flutter mobile application designed for studying, practicing, and mastering the **Constitution of the Republic of Kazakhstan** (*Қазақстан Республикасының Конституциясы*). 

Built with a **Clean Architecture + Feature-First** approach, ZanTest provides interactive quizzes, simulated civil service exams, detailed explanations, and offline functionality.

---

## 🌟 Key Features

* **Categorized Learning:** Practice questions structured by all 9 sections and 98 articles of the RK Constitution.
* **Civil Service Exam Simulator:** Timed mock exams designed to simulate real Kazakhstan government hiring tests.
* **Offline-First Storage:** Local database integration ensuring full offline access to all questions and study progress.
* **Instant Feedback & References:** Detailed explanations with direct citations to specific constitutional articles for every question.
* **Progress Tracking & Analytics:** Real-time stats on completed quizzes, accuracy rates, and weak areas.
* **Modern Kazakh Design System:** Clean, accessible UI inspired by national colors with dark/light mode support.

---

## 🛠 Tech Stack & Architecture

ZanTest is built following **Clean Architecture** combined with a **Feature-First** directory structure for scalability and maintainability.

* **Framework:** [Flutter](https://flutter.dev/) (Dart)
* **State Management:** [BLoC / Cubit](https://pub.dev/packages/flutter_bloc)
* **Local Database:** [Isar DB](https://pub.dev/packages/isar) (Fast, reactive offline-first storage)
* **Navigation:** [GoRouter](https://pub.dev/packages/go_router)
* **Typography & UI:** [Google Fonts](https://pub.dev/packages/google_fonts)
* **Equality & Immutability:** [Equatable](https://pub.dev/packages/equatable)

---

## 📁 Project Structure

```text
lib/
├── app/
│   ├── app.dart                  # MaterialApp initialization & Router setup
│   └── theme/                    # Color schemes, typography & themes
├── core/
│   ├── constants/                # App constants, article references, routes
│   ├── services/                 # Database initialization & local cache
│   └── utils/                    # Helper functions & formatters
└── features/
    ├── home/                     # Section selection & dashboard
    │   └── presentation/
    ├── quiz/                     # Core quiz engine
    │   ├── data/                 # Data sources, DTOs & Isar models
    │   ├── domain/               # Entities, repositories & use cases
    │   └── presentation/         # QuizBloc, quiz screens & dynamic widgets
    └── statistics/               # User analytics & exam results
        └── presentation/
        