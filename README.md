
<p align="center">
  <img width="100%" src="https://capsule-render.vercel.app/api?type=waving&color=0:141E30,100:243B55&height=220&section=header&text=Angular%20SSR%20eCommerce&fontSize=45&fontColor=ffffff" />
</p>

<h2 align="center">🛍️ Angular 17 SSR eCommerce Platform</h2>

<p align="center">
  🚀 Production Ready • Scalable • Clean Architecture
</p>

<p align="center">
  <a href="#"><img src="https://img.shields.io/badge/Live-Demo-blue?style=for-the-badge&logo=vercel" /></a>
  <a href="#"><img src="https://img.shields.io/badge/GitHub-Repo-black?style=for-the-badge&logo=github" /></a>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Angular-17-red?style=for-the-badge&logo=angular" />
  <img src="https://img.shields.io/badge/SSR-Enabled-blue?style=for-the-badge" />
  <img src="https://img.shields.io/badge/TailwindCSS-Styled-38B2AC?style=for-the-badge&logo=tailwindcss" />
  <img src="https://img.shields.io/badge/Auth-JWT-green?style=for-the-badge" />
  <img src="https://img.shields.io/badge/Status-Production--Ready-success?style=for-the-badge" />
</p>

---

## 🧠 About The Project

A **production-ready eCommerce frontend** built using **Angular 17 with Server-Side Rendering (SSR)**.

✔️ Authentication  
✔️ Product handling  
✔️ Cart system  
✔️ SSR optimization  

---

## 🖼️ Screenshots

<p align="center">
  <img src="https://via.placeholder.com/800x400?text=Home+Page" width="80%" />
  <img src="https://via.placeholder.com/800x400?text=Product+Page" width="80%" />
  <img src="https://via.placeholder.com/800x400?text=Cart+Page" width="80%" />
</p>

---

## 📦 Project Structure

```
eCommerceAngular/
├── src/
│   ├── app/
│   │   ├── layout/           # Pages and components (home, login, register, cart...)
│   │   ├── shared/           # Services, interfaces, guards
│   │   └── app.routes.ts     # All route definitions
├── server.ts                 # Express SSR entry point
├── angular.json              # Angular CLI config
├── package.json              # Dependencies & scripts
```

---

## 🚀 Features

- ✅ Angular 17 (Standalone Components + Server-Side Rendering)
- 🔐 JWT Authentication with route protection
- 🛒 Shopping Cart with persistent storage
- 📃 Reactive Forms with validation (Login/Register)
- 📦 Tailwind CSS + Flowbite UI components
- 🔔 Toast notifications (ngx-toastr)
- 📄 PDF Export support (html2pdf.js)

---

## 📥 Installation

1. Clone the repository:

```bash
git clone https://github.com/muhammed-alateeqi1/eCommerceAngular.git
cd eCommerceAngular
```

2. Install dependencies:

```bash
npm install
```

3. Run the development server:

```bash
npm start
```

---

## 🖥️ SSR & Production Build

To build and run the application with SSR:

```bash
npm run build
npm run serve:ssr:eCommerceSession
```

App will be available at: `http://localhost:4000`

---

## 🌐 Environment Configuration

API configuration is located in:

```bash
src/app/base/Environment.ts
```

> ✅ In production, you should:
> - Replace static `Environment.baseUrl` with `.env` support (using dotenv in server.ts)
> - Use different environments (`environment.prod.ts`)

---

## 🔐 Authentication
- JWT stored in `localStorage`
- AuthGuard checks login state
- Token is decoded via `jwt-decode` to extract user identity
- BehaviorSubject is used to hold logged-in user info
---

## ⚠️ Security Recommendations (Pre-Production)

> ✔️ = Implemented
> ❗ = Highly recommended
> 🔄 = Suggested enhancement

| Recommendation | Status | Notes |
|----------------|--------|-------|
| Remove `console.log` in production code | ✔️ | Already removed from login/register/services |
| Verify JWT expiration in `auth.guard.ts` | ✔️ | Patched with `exp` check |
| Avoid relying on `localStorage` for token | ❗ | Use `HttpOnly` cookies via backend instead |
| Use Express middleware: `helmet`, `cors`, `rate-limit` | ❗ | Add to `server.ts` for added protection |
| Sanitize user inputs | 🔄 | Add `ngx-mask` or Angular sanitizers where needed |
| Avoid direct use of `headers.host` in SSR engine | ❗ | Use a trusted `BASE_URL` instead |
| Apply Content Security Policy (CSP) | 🔄 | Set strict headers in Express |
| SSR file path safety | ✔️ | SSR static serving is safe but should validate base paths |
| No API keys or secrets in frontend | ✔️ | All API endpoints are generic |
| Avoid CDN for critical assets | 🔄 | Move FontAwesome to local assets for reliability and control |

---

## ✨ UI Technologies

- Tailwind CSS + Flowbite
- Font Awesome Icons
- Responsive design
- Toast feedback (ngx-toastr)

---



> Coverage and e2e testing are recommended for production.

---

## 📌 Suggested Improvements

- [ ] Angular HTTP Interceptor for auth token injection
- [ ] Use Angular environments + .env file for configs
- [ ] Implement lazy loading for cart/products modules
- [ ] Add logout auto-expiry via token `exp`
- [ ] Translate form & alert messages (i18n)
- [ ] Optimize SSR render for speed with static generation

---

## 👤 Author

Developed by [Muhammed Al-Ateeqi](https://github.com/muhammed-alateeqi1)  
📧 Email: mu.alateeqi@gmail.com

---

## 📄 License

MIT License

---

## 📚 Documentation & Contribution

For documentation updates or to contribute:

1. Fork this repository
2. Create a new feature branch
3. Submit pull request

For API specs or architecture diagram, refer to the `/docs` directory (to be created).

