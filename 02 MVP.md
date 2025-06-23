## 🚀 Цель MVP
Создать MVP цифровой платформы, обеспечивающей прозрачный, структурированный и гибкий процесс периодической оценки сотрудников

---
## 👣 MVP User Flow
- Админ создаёт компанию и назначает в неё HR
- HR настраивает департаменты и иерархию
- HR создаёт новый [период оценивания](период%20оценивания.md)
- HR создаёт [шаблон анкеты](шаблон%20анкеты.md) для периода
- Сотрудник получает уведомление на почту и регистрируется
- Сотрудник заполняет анкету
- Менеджер добавляет комментарии по анкете
- Менеджер создаёт сводку по команде

---
## 🖼️ Примеры прототипов  
- [Пример анкеты](self-review-form.md)
- [Пример dashboard HR](dashboard-hr.md)
- [Пример dashboard менеджера](dashboard-manager.md)
- [Пример сводки по команде](Prototype/team-summary.md)

---
## 📦 MVP Epics
### 📦 Epic 1: Инициализация
#### User Stories
- Как системный администратор, я хочу создать/сконфигурировать пользователя
- Как администратор, я хочу создать/изменить/удалить компанию
- Как администратор, я хочу создать HR-пользователя для компании
- Как пользователь, я хочу получить письмо для первого входа
- Как пользователь, я хочу зайти в систему
- Как сотрудник, я хочу увидеть приветствие сотрудника после входа
- Как менеджер, я хочу увидеть приветствие менеджера после входа
- Как HR, я хочу увидеть приветствие HRа после входа
- Как администратор, я хочу увидеть приветствие администратора после входа
- Как пользователь, я хочу сменить пароль
- Как пользователь, я хочу восстановить пароль
- Как пользователь, я хочу выйти из систему
- Как пользователь, я хочу восстановить пароль через email
#### Tasks
- Создание проекта
- CRUD компаний
- CRUD пользователей
- Роли
- Авторизация
- Аудит лог
- Email-нотификации
- Профиль
- Восстановление пароля
### 📦 Epic 2: HR-конфигурация
#### User Stories
- Как HR, я хочу создать/отредактировать/удалить департаменты
- Как HR, я хочу привязать пользователей к департаментам и настроить иерархию
- Как HR, я хочу создать/отредактировать/удалить период оценивания
- Как HR, я хочу создать/отредактировать/удалить шаблон анкеты
- Как HR, я хочу создать/отредактировать/удалить вопросы для шаблона анкеты
#### Tasks
- HR-dashboard
- CRUD департаментов
- Настройка иерархии пользователей
- CRUD периодов
- CRUD шаблонов анкет
- CRUD вопросов
### 📦 Epic 3: Заполнение анкет
#### User Stories
- Как сотрудник, я хочу увидеть информацию о текущем периоде на dashboard странице
- Как сотрудник, я хочу ввести/изменить ответы на вопросы анкеты за текущий период
- Как сотрудник, я хочу увидеть анкеты и ответы за предыдущие периоды на dashboard странице
- Как сотрудник, я хочу увидеть публичные комментарии менеджера по моей анкете
- Как менеджер, я хочу увидеть список сотрудников и статусы заполнения анкет на dashboard странице
- Как менеджер, я хочу увидеть ответы сотрудника по анкете
- Как менеджер, я хочу добавить публичные комментарии по ответам сотрудника в анкете
- Как менеджер, я хочу добавить приватные комментарии по ответам сотрудника в анкете
- Как менеджер, я хочу просмотреть предыдущие анкеты сотрудника
- Как менеджер, я хочу создать/отредактировать сводку по команде за текущий период оценивания
- Как менеджер, я хочу иметь функционал сотрудника, чтобы заполнить анкету для моего менеджера
#### Tasks
- Dashboard
- CRUD ответов для сотрудников
- CRUD комментариев для менеджеров
- CRUD сводок по команде для менеджеров
### 📦 Epic 4: HR-dashboard
#### User Stories
- Как HR, я хочу видеть список всех периодов и заходить в любой из них
- Как HR, я хочу видеть прогресс по заполнению анкет по департаментам за конкретный период
- Как HR, я хочу видеть прогресс по заполнению анкет сотрудниками из конкретного департаментов
- Как HR, я хочу видеть ответы сотрудника, публичные и приватные комментарии менеджера.
- Как HR, я хочу видеть сводки по команде
#### Tasks
- Список периодов
- Список департаментов
- Список сотрудников
- Просмотре анкеты и комментариев
- Просмотре сводки по команде

---
## 🗺️ Карта интерфейсов (UI Map)
### 1. 🔐 Аутентификация (все роли)
- **Login Page**
- **Reset Password Page**
- **Set New Password Page**
- **First Login Invitation Page**
- **Change Password Page**
- **Logout Button**
### 2. 🛠️ Администратор
#### Главная: **Admin Dashboard**
-  Список компаний
    - ➕ Создать / ✏️ Редактировать / 🗑️ Удалить
-  Пользователи
    - ➕ Создать HR
    - 📧 Отправить приглашение
    - 🧾 Аудит лог по действиям пользователей
-  Профиль администратора
### 3. 🧑‍💼 HR
#### Главная: **HR Dashboard**
-  📁 Управление департаментами
    - ➕ Создать / ✏️ Редактировать / 🗑️ Удалить
-  🧭 Иерархия сотрудников
    - Drag & Drop / дерево / список
-  📅 Периоды оценивания
    - ➕ Новый период
    - 📄 Детали периода → шаблон, статус заполнения
-  🧩 Шаблоны анкет
    - ➕ Новый шаблон
    - 📝 Редактировать / удалить вопросы
-  👀 Мониторинг прогресса
    - Список периодов
    - Выбор департамента → список сотрудников
        - Статус заполнения
        - Просмотр ответов
        - Просмотр комментариев
        - Просмотр сводок по команде
-  Профиль HR
### 4. 👨‍💻 Сотрудник
#### Главная: **Employee Dashboard**
-  📌 Текущий период оценивания
    - 📝 Заполнить анкету
    - ✏️ Изменить до дедлайна
-  📜 История анкет
    - Периоды → анкеты → ответы
    - Комментарии менеджера (публичные)
-  👤 Профиль сотрудника
### 5. 👨‍💼 Менеджер
#### Главная: **Manager Dashboard**
-  👥 Список сотрудников команды
    - Статус анкет
    - Просмотр анкеты
        - Добавление комментариев (публичные/приватные)
        - История анкет
-  📊 Сводка по команде
    - ➕ Создать
    - ✏️ Редактировать
-  📝 Анкета для своего менеджера (как сотрудник)
-  Профиль менеджера
## 🔄 Общие компоненты
- **Header**
    - Навигация (в зависимости от роли)
    - Профиль
    - Выход
- **Notifications (email + UI):**
    - Приглашение
    - Напоминание о заполнении
    - Обновление статуса периода
- **Error Pages** (403, 404, 500)

---
## 🧭 Пример навигации по ролям

| Роль      | Главный экран      | Допуск к            | Специализированные функции |
| --------- | ------------------ | ------------------- | -------------------------- |
| Админ     | Admin Dashboard    | Компании, HR        | Управление структурами     |
| HR        | HR Dashboard       | Всё внутри компании | Конфигурация, контроль     |
| Менеджер  | Manager Dashboard  | Только своя команда | Комментарии, сводки        |
| Сотрудник | Employee Dashboard | Только свои данные  | Заполнение анкет           |

---
## 🗄️ Пример структуры базы
### ✅ Company Entity

```php
// src/Entity/Company.php
namespace App\Entity;

use App\Repository\CompanyRepository;
use Doctrine\ORM\Mapping as ORM;

#[ORM\Entity(repositoryClass: CompanyRepository::class)]
class Company
{
    #[ORM\Id]
    #[ORM\GeneratedValue]
    #[ORM\Column]
    private ?int $id = null;

    #[ORM\Column(length: 255)]
    private ?string $name = null;

    #[ORM\Column(length: 255, nullable: true)]
    private ?string $domain = null;

    // ...
}
```
### ✅ User Entity

```php
// src/Entity/User.php
namespace App\Entity;

use App\Repository\UserRepository;
use Doctrine\ORM\Mapping as ORM;

#[ORM\Entity(repositoryClass: UserRepository::class)]
class User
{
    #[ORM\Id]
    #[ORM\GeneratedValue]
    #[ORM\Column]
    private ?int $id = null;

    #[ORM\Column(length: 180, unique: true)]
    private ?string $email = null;

    #[ORM\Column]
    private array $roles = [];

    #[ORM\Column(length: 255)]
    private ?string $password = null;

    #[ORM\Column(length: 255)]
    private ?string $name = null;

    #[ORM\ManyToOne(inversedBy: 'users')]
    private ?Company $company = null;

    #[ORM\ManyToOne]
    private ?Department $department = null;

    #[ORM\ManyToOne]
    private ?User $manager = null;

    // ...
}
```
### ✅ Department Entity

```php
// src/Entity/Department.php
namespace App\Entity;

use App\Repository\DepartmentRepository;
use Doctrine\ORM\Mapping as ORM;

#[ORM\Entity(repositoryClass: DepartmentRepository::class)]
class Department
{
    #[ORM\Id]
    #[ORM\GeneratedValue]
    #[ORM\Column]
    private ?int $id = null;

    #[ORM\Column(length: 255)]
    private ?string $name = null;

    #[ORM\ManyToOne]
    private ?Company $company = null;
}
```
### ✅ ReviewPeriod Entity

```php
// src/Entity/ReviewPeriod.php
namespace App\Entity;

use App\Repository\ReviewPeriodRepository;
use Doctrine\ORM\Mapping as ORM;

#[ORM\Entity(repositoryClass: ReviewPeriodRepository::class)]
class ReviewPeriod
{
    #[ORM\Id]
    #[ORM\GeneratedValue]
    #[ORM\Column]
    private ?int $id = null;

    #[ORM\Column(length: 255)]
    private ?string $title = null;

    #[ORM\Column(type: 'datetime')]
    private ?\DateTimeInterface $startDate = null;

    #[ORM\Column(type: 'datetime')]
    private ?\DateTimeInterface $endDate = null;

    #[ORM\ManyToOne]
    private ?Company $company = null;
}
```
### ✅ SurveyTemplate Entity

```php
// src/Entity/SurveyTemplate.php
namespace App\Entity;

use App\Repository\SurveyTemplateRepository;
use Doctrine\ORM\Mapping as ORM;

#[ORM\Entity(repositoryClass: SurveyTemplateRepository::class)]
class SurveyTemplate
{
    #[ORM\Id]
    #[ORM\GeneratedValue]
    #[ORM\Column]
    private ?int $id = null;

    #[ORM\Column(length: 255)]
    private ?string $title = null;

    #[ORM\ManyToOne]
    private ?ReviewPeriod $period = null;
}
```
### ✅ Question Entity

```php
// src/Entity/Question.php
namespace App\Entity;

use App\Repository\QuestionRepository;
use Doctrine\ORM\Mapping as ORM;

#[ORM\Entity(repositoryClass: QuestionRepository::class)]
class Question
{
    #[ORM\Id]
    #[ORM\GeneratedValue]
    #[ORM\Column]
    private ?int $id = null;

    #[ORM\Column(length: 1000)]
    private ?string $text = null;

    #[ORM\ManyToOne]
    private ?SurveyTemplate $template = null;
}
```
### ✅ SurveyAnswer Entity

```php
// src/Entity/SurveyAnswer.php
namespace App\Entity;

use App\Repository\SurveyAnswerRepository;
use Doctrine\ORM\Mapping as ORM;

#[ORM\Entity(repositoryClass: SurveyAnswerRepository::class)]
class SurveyAnswer
{
    #[ORM\Id]
    #[ORM\GeneratedValue]
    #[ORM\Column]
    private ?int $id = null;

    #[ORM\Column(type: 'text')]
    private ?string $answer = null;

    #[ORM\ManyToOne]
    private ?Question $question = null;

    #[ORM\ManyToOne]
    private ?User $employee = null;

    #[ORM\ManyToOne]
    private ?ReviewPeriod $period = null;
}
```
### ✅ Comment Entity

```php
// src/Entity/Comment.php
namespace App\Entity;

use App\Repository\CommentRepository;
use Doctrine\ORM\Mapping as ORM;

#[ORM\Entity(repositoryClass: CommentRepository::class)]
class Comment
{
    #[ORM\Id]
    #[ORM\GeneratedValue]
    #[ORM\Column]
    private ?int $id = null;

    #[ORM\Column(type: 'text')]
    private ?string $text = null;

    #[ORM\Column]
    private bool $isPrivate = false;

    #[ORM\ManyToOne]
    private ?User $manager = null;

    #[ORM\ManyToOne]
    private ?SurveyAnswer $answer = null;
}
```
### ✅ TeamSummary Entity

```php
// src/Entity/TeamSummary.php
namespace App\Entity;

use App\Repository\TeamSummaryRepository;
use Doctrine\ORM\Mapping as ORM;

#[ORM\Entity(repositoryClass: TeamSummaryRepository::class)]
class TeamSummary
{
    #[ORM\Id]
    #[ORM\GeneratedValue]
    #[ORM\Column]
    private ?int $id = null;

    #[ORM\Column(type: 'text')]
    private ?string $summary = null;

    #[ORM\ManyToOne]
    private ?User $manager = null;

    #[ORM\ManyToOne]
    private ?ReviewPeriod $period = null;
}
```
