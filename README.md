# Kloud Course Academy Project Structure

```text
kloud-course-academy/
├── public/                       # Static assets, favicon, logo
│
├── src/
│   ├── api/                      # Axios instances + API callers
│   │   ├── axiosInstance.js
│   │   ├── authApi.js
│   │   ├── courseApi.js
│   │   ├── quizApi.js
│   │   ├── blogApi.js
│   │   ├── paymentApi.js
│   │   └── uploadApi.js          # S3 presigned upload helpers
│   │
│   ├── assets/                   # Images, fonts, icons
│   │   ├── fonts/
│   │   ├── images/
│   │   └── icons/
│   │
│   ├── components/               # Shared / reusable UI
│   │   ├── common/
│   │   │   ├── Navbar.jsx
│   │   │   ├── Footer.jsx
│   │   │   ├── Breadcrumb.jsx
│   │   │   ├── Loader.jsx
│   │   │   ├── Modal.jsx
│   │   │   ├── Toast.jsx
│   │   │   ├── SEOHead.jsx
│   │   │   └── ProtectedRoute.jsx
│   │   │
│   │   ├── ui/                   # Design system atoms
│   │   │   ├── Button.jsx
│   │   │   ├── Input.jsx
│   │   │   ├── Card.jsx
│   │   │   ├── Badge.jsx
│   │   │   ├── Avatar.jsx
│   │   │   ├── Tabs.jsx
│   │   │   ├── Accordion.jsx
│   │   │   └── ProgressBar.jsx
│   │   │
│   │   ├── course/
│   │   │   ├── CourseCard.jsx
│   │   │   ├── CourseGrid.jsx
│   │   │   ├── CourseFilters.jsx
│   │   │   ├── CourseHero.jsx
│   │   │   ├── CurriculumAccordion.jsx
│   │   │   ├── InstructorCard.jsx
│   │   │   ├── ReviewSection.jsx
│   │   │   └── VideoPlayer.jsx   # CloudFront-signed URL player
│   │   │
│   │   ├── lms/
│   │   │   ├── LessonSidebar.jsx
│   │   │   ├── LessonContent.jsx
│   │   │   ├── ProgressTracker.jsx
│   │   │   ├── NotesTaker.jsx
│   │   │   └── CertificateCard.jsx
│   │   │
│   │   ├── quiz/
│   │   │   ├── QuizRunner.jsx
│   │   │   ├── QuestionCard.jsx
│   │   │   ├── QuizTimer.jsx
│   │   │   ├── QuizResults.jsx
│   │   │   └── ExamProctor.jsx
│   │   │
│   │   ├── blog/
│   │   │   ├── BlogCard.jsx
│   │   │   ├── BlogGrid.jsx
│   │   │   └── RichTextRenderer.jsx
│   │   │
│   │   ├── payment/
│   │   │   ├── RazorpayButton.jsx
│   │   │   ├── PricingCard.jsx
│   │   │   ├── OrderSummary.jsx
│   │   │   └── CouponInput.jsx
│   │   │
│   │   └── events/
│   │       ├── EventCard.jsx
│   │       └── EventBanner.jsx
│   │
│   ├── pages/
│   │   ├── public/               # No auth required
│   │   │   ├── Home.jsx
│   │   │   ├── Courses.jsx
│   │   │   ├── CourseDetail.jsx
│   │   │   ├── InstructorLed.jsx
│   │   │   ├── LearningPath.jsx
│   │   │   ├── JobRoleLearning.jsx
│   │   │   ├── Blog.jsx
│   │   │   ├── BlogPost.jsx
│   │   │   ├── Events.jsx
│   │   │   ├── EventDetail.jsx
│   │   │   ├── HireFromUs.jsx
│   │   │   ├── Careers.jsx
│   │   │   ├── Internship.jsx
│   │   │   ├── Hackathons.jsx
│   │   │   ├── Apprenticeship.jsx
│   │   │   ├── ForInstitutions.jsx
│   │   │   ├── ForGovernments.jsx
│   │   │   ├── About.jsx
│   │   │   ├── Contact.jsx
│   │   │   └── NotFound.jsx
│   │   │
│   │   ├── auth/
│   │   │   ├── Login.jsx
│   │   │   ├── Register.jsx
│   │   │   ├── ForgotPassword.jsx
│   │   │   └── ResetPassword.jsx
│   │   │
│   │   ├── learner/              # Authenticated student
│   │   │   ├── Dashboard.jsx
│   │   │   ├── MyCourses.jsx
│   │   │   ├── Learn.jsx
│   │   │   ├── Quizzes.jsx
│   │   │   ├── Certificates.jsx
│   │   │   ├── Orders.jsx
│   │   │   └── Profile.jsx
│   │   │
│   │   ├── trainer/              # Authenticated instructor
│   │   │   ├── Dashboard.jsx
│   │   │   ├── MyCourses.jsx
│   │   │   ├── CourseBuilder.jsx
│   │   │   ├── LessonEditor.jsx
│   │   │   ├── QuizBuilder.jsx
│   │   │   ├── Students.jsx
│   │   │   ├── Earnings.jsx
│   │   │   └── Profile.jsx
│   │   │
│   │   └── admin/                # Super admin
│   │       ├── Dashboard.jsx
│   │       ├── AllCourses.jsx
│   │       ├── AllUsers.jsx
│   │       ├── BlogManager.jsx
│   │       ├── EventManager.jsx
│   │       ├── Payments.jsx
│   │       ├── Categories.jsx
│   │       ├── Coupons.jsx
│   │       ├── Subscribers.jsx
│   │       └── Settings.jsx
│   │
│   ├── layouts/
│   │   ├── PublicLayout.jsx
│   │   ├── AuthLayout.jsx
│   │   ├── LearnerLayout.jsx
│   │   ├── TrainerLayout.jsx
│   │   └── AdminLayout.jsx
│   │
│   ├── routes/
│   │   ├── index.jsx             # React Router v6 root
│   │   ├── publicRoutes.jsx
│   │   ├── authRoutes.jsx
│   │   ├── learnerRoutes.jsx
│   │   ├── trainerRoutes.jsx
│   │   └── adminRoutes.jsx
│   │
│   ├── store/                    # Redux Toolkit / Zustand
│   │   ├── index.js
│   │   ├── authSlice.js
│   │   ├── courseSlice.js
│   │   ├── cartSlice.js
│   │   ├── uiSlice.js
│   │   └── quizSlice.js
│   │
│   ├── hooks/                    # Custom React hooks
│   │   ├── useAuth.js
│   │   ├── useCourseProgress.js
│   │   ├── useRazorpay.js
│   │   ├── useS3Upload.js
│   │   ├── useQuiz.js
│   │   └── useDebounce.js
│   │
│   ├── context/
│   │   ├── AuthContext.jsx
│   │   └── ThemeContext.jsx
│   │
│   ├── utils/
│   │   ├── formatters.js
│   │   ├── validators.js
│   │   ├── constants.js
│   │   ├── cloudfront.js         # Signed URL generator
│   │   ├── razorpay.js
│   │   └── permissions.js
│   │
│   ├── styles/
│   │   ├── globals.css           # CSS variables, reset
│   │   ├── typography.css
│   │   ├── components.css
│   │   └── theme.css             # Light / dark tokens
│   │
│   ├── config/
│   │   ├── env.js
│   │   ├── s3Config.js
│   │   ├── razorpayConfig.js
│   │   └── routes.js             # Route constants
│   │
│   ├── App.jsx
│   └── main.jsx
│
├── .env.example
├── .eslintrc.cjs
├── vite.config.js
├── tailwind.config.js
└── package.json
