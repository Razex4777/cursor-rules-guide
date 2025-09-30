# 🎯 دليل شامل لقواعد Cursor IDE

## 📋 نظرة عامة

**Cursor Rules** هي ميزة متقدمة في محرر Cursor IDE تسمح للمطورين بتعريف قواعد مخصصة لمساعد الذكاء الاصطناعي. هذه القواعد تساعد في تخصيص سلوك المساعد ليتوافق مع احتياجات المشروع المحددة.

---

## 🎨 ما هي قواعد Cursor؟

### ✨ التعريف
قواعد Cursor هي ملفات نصية تحتوي على تعليمات مخصصة لمساعد الذكاء الاصطناعي في Cursor IDE. هذه القواعد تساعد في:

- 🎯 **تخصيص سلوك المساعد** حسب احتياجات المشروع
- 📝 **تحسين جودة الكود** المولد
- 🔧 **تطبيق معايير محددة** للفريق
- 🚀 **تسريع عملية التطوير**

### 📁 الملفات المطلوبة
```
.cursorrules          # الملف الرئيسي للقواعد
.cursor/              # مجلد إضافي للقواعد المتقدمة
.cursorignore         # ملف لتجاهل ملفات معينة
```

---

## 🛠️ إنشاء ملف .cursorrules

### 📝 البنية الأساسية

```markdown
# قواعد المشروع
You are an expert developer working on [PROJECT_NAME].

## 🎯 الهدف
[وصف الهدف من المشروع]

## 📋 القواعد العامة
- استخدم [LANGUAGE] للبرمجة
- اتبع معايير [STANDARDS]
- ركز على [FOCUS_AREA]

## 🔧 التطوير
- استخدم [FRAMEWORK]
- اتبع نمط [PATTERN]
- طبق [PRINCIPLES]

## 📁 هيكل المشروع
```
src/
├── components/
├── pages/
├── utils/
└── styles/
```

## 🎨 التصميم
- استخدم [DESIGN_SYSTEM]
- طبق [UI_FRAMEWORK]
- اتبع [STYLING_APPROACH]
```

---

## 🎯 أمثلة عملية للقواعد

### 1. 🚀 مشروع React/TypeScript

```markdown
# قواعد مشروع React
You are a senior React developer working on a modern web application.

## 🎯 الهدف
بناء تطبيق ويب حديث باستخدام React و TypeScript

## 📋 القواعد العامة
- استخدم TypeScript دائماً
- اتبع React Hooks patterns
- طبق Clean Code principles
- ركز على Performance optimization

## 🔧 التطوير
- استخدم Functional Components
- طبق Custom Hooks للـ logic
- استخدم Context API للـ state management
- طبق Error Boundaries

## 📁 هيكل المشروع
```
src/
├── components/          # مكونات قابلة للإعادة
├── pages/              # صفحات التطبيق
├── hooks/              # Custom Hooks
├── context/            # React Context
├── utils/              # Utility functions
└── types/              # TypeScript types
```

## 🎨 التصميم
- استخدم Tailwind CSS
- طبق shadcn/ui components
- اتبع Mobile-first approach
- استخدم Responsive design

## 📝 أمثلة الكود
```tsx
// ✅ صحيح
const MyComponent: React.FC<Props> = ({ title, onClick }) => {
  const [state, setState] = useState<string>('');
  
  return (
    <div className="p-4 bg-white rounded-lg">
      <h2>{title}</h2>
      <button onClick={onClick}>Click me</button>
    </div>
  );
};

// ❌ خطأ
function MyComponent(props) {
  return <div>{props.title}</div>;
}
```
```

### 2. 🎨 مشروع UI/UX Design

```markdown
# قواعد تصميم UI/UX
You are a UI/UX designer and developer working on modern web interfaces.

## 🎯 الهدف
إنشاء واجهات مستخدم جميلة وسهلة الاستخدام

## 📋 القواعد العامة
- اتبع Material Design principles
- طبق Accessibility standards (WCAG 2.1)
- ركز على User Experience
- استخدم Consistent design patterns

## 🎨 التصميم
- استخدم Design System موحد
- طبق Color palette محددة
- استخدم Typography hierarchy
- طبق Spacing system

## 📱 Responsive Design
- Mobile-first approach
- Breakpoints: sm, md, lg, xl
- Flexible layouts
- Touch-friendly interfaces

## ♿ Accessibility
- Semantic HTML
- ARIA labels
- Keyboard navigation
- Screen reader support
- Color contrast ratio 4.5:1

## 🎯 أمثلة التصميم
```css
/* ✅ صحيح - Design System */
.button-primary {
  background: var(--primary-color);
  padding: 12px 24px;
  border-radius: 8px;
  font-weight: 600;
  transition: all 0.2s ease;
}

/* ❌ خطأ - بدون نظام */
.btn {
  background: blue;
  padding: 10px;
}
```
```

### 3. 🔧 مشروع Backend/API

```markdown
# قواعد Backend Development
You are a backend developer working on RESTful APIs and server-side applications.

## 🎯 الهدف
بناء APIs آمنة وقابلة للتوسع

## 📋 القواعد العامة
- استخدم Node.js/Express
- طبق RESTful API principles
- ركز على Security
- استخدم Database best practices

## 🔧 التطوير
- استخدم TypeScript للـ type safety
- طبق Error handling شامل
- استخدم Validation middleware
- طبق Authentication & Authorization

## 🗄️ Database
- استخدم PostgreSQL/MySQL
- طبق Database migrations
- استخدم ORM (Prisma/TypeORM)
- طبق Database indexing

## 🔒 Security
- استخدم HTTPS دائماً
- طبق Input validation
- استخدم Rate limiting
- طبق CORS policies
- استخدم Environment variables

## 📝 أمثلة الكود
```typescript
// ✅ صحيح - API Route
export async function POST(request: Request) {
  try {
    const body = await request.json();
    
    // Validation
    const validatedData = schema.parse(body);
    
    // Business logic
    const result = await createUser(validatedData);
    
    return Response.json({ success: true, data: result });
  } catch (error) {
    return Response.json(
      { error: 'Invalid request' },
      { status: 400 }
    );
  }
}
```
```

---

## 🎯 أنواع القواعد المختلفة

### 1. 📝 قواعد البرمجة

```markdown
## 🐍 Python Rules
- استخدم type hints دائماً
- طبق PEP 8 standards
- استخدم async/await للـ I/O operations
- طبق Error handling شامل

## ☕ Java Rules
- استخدم Spring Boot framework
- طبق SOLID principles
- استخدم Dependency Injection
- طبق Clean Architecture

## 🦀 Rust Rules
- استخدم Ownership system
- طبق Memory safety
- استخدم Pattern matching
- طبق Error handling مع Result<T, E>
```

### 2. 🎨 قواعد التصميم

```markdown
## 🎨 Design System Rules
- استخدم Consistent color palette
- طبق Typography scale
- استخدم Spacing system
- طبق Component library

## 📱 Mobile Rules
- استخدم Touch-friendly targets (44px min)
- طبق Gesture-based interactions
- استخدم Platform-specific patterns
- طبق Performance optimization
```

### 3. 🔧 قواعد DevOps

```markdown
## 🐳 Docker Rules
- استخدم Multi-stage builds
- طبق Security best practices
- استخدم .dockerignore
- طبق Health checks

## ☸️ Kubernetes Rules
- استخدم Resource limits
- طبق Security contexts
- استخدم ConfigMaps للـ configuration
- طبق Rolling updates
```

---

## 🚀 أمثلة متقدمة للقواعد

### 1. 🎯 مشروع Full-Stack

```markdown
# قواعد مشروع Full-Stack
You are a full-stack developer working on a modern web application.

## 🎯 الهدف
بناء تطبيق ويب كامل مع Frontend و Backend

## 🏗️ Architecture
- Frontend: React + TypeScript + Tailwind
- Backend: Node.js + Express + TypeScript
- Database: PostgreSQL + Prisma
- Authentication: JWT + bcrypt
- Deployment: Docker + Vercel

## 📁 هيكل المشروع
```
project/
├── frontend/           # React app
│   ├── src/
│   │   ├── components/
│   │   ├── pages/
│   │   ├── hooks/
│   │   └── utils/
│   └── package.json
├── backend/            # Node.js API
│   ├── src/
│   │   ├── routes/
│   │   ├── middleware/
│   │   ├── models/
│   │   └── utils/
│   └── package.json
├── shared/            # Shared types
└── docker-compose.yml
```

## 🔧 Development Rules
- استخدم Monorepo structure
- طبق Shared TypeScript types
- استخدم ESLint + Prettier
- طبق Git hooks مع Husky

## 🎨 Frontend Rules
- استخدم React 18+ features
- طبق Custom hooks للـ logic
- استخدم React Query للـ data fetching
- طبق Error boundaries

## 🔧 Backend Rules
- استخدم Express.js framework
- طبق RESTful API design
- استخدم Prisma ORM
- طبق JWT authentication

## 📝 أمثلة الكود
```typescript
// Frontend - Custom Hook
export const useUsers = () => {
  const { data, isLoading, error } = useQuery({
    queryKey: ['users'],
    queryFn: fetchUsers,
  });

  return { users: data, isLoading, error };
};

// Backend - API Route
export const getUsers = async (req: Request, res: Response) => {
  try {
    const users = await prisma.user.findMany();
    res.json({ success: true, data: users });
  } catch (error) {
    res.status(500).json({ error: 'Internal server error' });
  }
};
```
```

### 2. 🎨 مشروع Design System

```markdown
# قواعد Design System
You are a design system architect working on a comprehensive component library.

## 🎯 الهدف
إنشاء نظام تصميم شامل ومتسق

## 🎨 Design Tokens
```css
/* Colors */
--primary-50: #f0f9ff;
--primary-500: #3b82f6;
--primary-900: #1e3a8a;

/* Typography */
--font-size-xs: 0.75rem;
--font-size-sm: 0.875rem;
--font-size-base: 1rem;

/* Spacing */
--space-1: 0.25rem;
--space-2: 0.5rem;
--space-4: 1rem;
```

## 🧩 Component Rules
- استخدم Atomic Design methodology
- طبق Accessibility standards
- استخدم Storybook للـ documentation
- طبق Testing مع Jest + Testing Library

## 📱 Responsive Rules
- Mobile-first approach
- Breakpoints: 320px, 768px, 1024px, 1440px
- Flexible grid system
- Touch-friendly interactions

## ♿ Accessibility Rules
- WCAG 2.1 AA compliance
- Keyboard navigation
- Screen reader support
- Color contrast 4.5:1 minimum
- Focus indicators
```

---

## 🎯 أفضل الممارسات

### 1. 📝 كتابة القواعد

```markdown
## ✅ نصائح للكتابة الجيدة

### 🎯 كن محدداً
❌ سيء: "اكتب كود جيد"
✅ جيد: "استخدم TypeScript، طبق Clean Code، ركز على Performance"

### 📋 استخدم التنسيق
- استخدم Headers للتنظيم
- طبق Bullet points للقوائم
- استخدم Code blocks للأمثلة
- طبق Emojis للوضوح

### 🔧 قدم أمثلة
```typescript
// ✅ مثال صحيح
const Button: React.FC<ButtonProps> = ({ 
  variant = 'primary', 
  size = 'medium',
  children,
  onClick 
}) => {
  return (
    <button 
      className={`btn btn-${variant} btn-${size}`}
      onClick={onClick}
    >
      {children}
    </button>
  );
};

// ❌ مثال خطأ
const Button = (props) => <button {...props} />;
```
```

### 2. 🎯 تنظيم القواعد

```markdown
## 📁 هيكل القواعد المثالي

```markdown
# 🎯 عنوان المشروع
وصف مختصر للمشروع

## 📋 القواعد العامة
- القواعد الأساسية
- المعايير المطلوبة
- الأهداف الرئيسية

## 🔧 التطوير
- Framework المستخدم
- Patterns المطلوبة
- Best practices

## 📁 هيكل المشروع
```
project/
├── src/
├── tests/
└── docs/
```

## 🎨 التصميم
- Design system
- UI framework
- Styling approach

## 📝 أمثلة الكود
```typescript
// أمثلة عملية
```

## 🚫 تجنب
- الأخطاء الشائعة
- Anti-patterns
- الممارسات السيئة
```
```

---

## 🚀 التطبيق العملي

### 1. 📁 إنشاء ملف .cursorrules

```bash
# إنشاء الملف
touch .cursorrules

# محتوى الملف
cat > .cursorrules << 'EOF'
# قواعد مشروع Khadum
You are an expert developer working on Khadum - a smart WhatsApp broker platform.

## 🎯 الهدف
بناء منصة ذكية تربط العملاء بالمستقلين عبر واتساب

## 📋 القواعد العامة
- استخدم React + TypeScript
- طبق Tailwind CSS للتصميم
- ركز على User Experience
- استخدم shadcn/ui components

## 🔧 التطوير
- استخدم Functional Components
- طبق Custom Hooks
- استخدم Context API
- طبق Error Boundaries

## 🎨 التصميم
- استخدم Premium light theme
- طبق Glass effects
- استخدم Responsive design
- طبق Micro-animations

## 📝 أمثلة الكود
```tsx
// ✅ صحيح
const HeroSection: React.FC = () => {
  return (
    <section className="bg-gradient-to-br from-primary to-primary-light">
      <div className="container mx-auto px-4">
        <h1 className="text-4xl font-bold text-white">
          مرحباً بك في خدوم
        </h1>
      </div>
    </section>
  );
};
```
EOF
```

### 2. 🎯 استخدام القواعد

```markdown
## 🔄 دورة العمل

1. **📝 كتابة القواعد** - تعريف المعايير المطلوبة
2. **🔧 تطبيق القواعد** - استخدامها في التطوير
3. **📊 مراجعة النتائج** - تقييم جودة الكود
4. **🔄 تحسين القواعد** - تحديث القواعد حسب الحاجة

## 🎯 النتائج المتوقعة

### ✅ فوائد القواعد
- 🚀 **تسريع التطوير** - كود أفضل وأسرع
- 🎯 **تحسين الجودة** - معايير موحدة
- 🔧 **سهولة الصيانة** - كود منظم
- 👥 **تعاون أفضل** - معايير واضحة

### 📊 مقاييس النجاح
- ⏱️ **وقت التطوير** - تقليل الوقت المطلوب
- 🐛 **عدد الأخطاء** - تقليل البق (bugs)
- 📈 **جودة الكود** - تحسين قابلية القراءة
- 👥 **رضا الفريق** - سهولة التعاون
```

---

## 🎯 الخلاصة

### ✨ ما تعلمناه

1. **🎯 تعريف القواعد** - ما هي وكيف تعمل
2. **📝 كتابة القواعد** - كيفية إنشاء قواعد فعالة
3. **🔧 التطبيق العملي** - أمثلة حقيقية
4. **🚀 أفضل الممارسات** - نصائح للنجاح

### 🎯 الخطوات التالية

1. **📝 ابدأ بسيط** - قواعد أساسية أولاً
2. **🔧 طبق تدريجياً** - أضف قواعد جديدة مع الوقت
3. **📊 راقب النتائج** - قيم تأثير القواعد
4. **🔄 حسّن باستمرار** - حدث القواعد حسب الحاجة

### 🎉 النتيجة النهائية

باستخدام قواعد Cursor بشكل صحيح، ستحصل على:
- 🚀 **تطوير أسرع** وأكثر كفاءة
- 🎯 **كود أفضل** وأكثر تنظيماً
- 👥 **تعاون أفضل** مع الفريق
- 📈 **نتائج أفضل** للمشروع

---

## 📚 مراجع إضافية

- [Cursor Documentation](https://cursor.sh/docs)
- [AI Coding Best Practices](https://cursor.sh/guides)
- [TypeScript Guidelines](https://typescriptlang.org/docs)
- [React Best Practices](https://react.dev/learn)

---

*تم إنشاء هذا الدليل لمساعدتك في فهم واستخدام قواعد Cursor بشكل فعال. استخدمه كمرجع في مشاريعك المستقبلية!* 🎯✨