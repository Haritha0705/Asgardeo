# Next.js Student Portal with Asgardeo Authentication

This is a **Next.js** web application demonstrating secure user authentication using **Asgardeo (WSO2 Identity Server)**. Users can register, log in, and access protected pages using OAuth2 / OpenID Connect tokens.

---

## Features

- **Next.js frontend** with SSR/CSR support  
- **User registration and login** via Asgardeo  
- OAuth2 / OpenID Connect authentication  
- Protected routes using **middleware**  
- Token validation on client and server  

---

## Requirements

- Node.js >= 18  
- npm or yarn  
- Asgardeo Developer Account ([https://wso2.com/asgardeo](https://wso2.com/asgardeo))  

---

## Setup

1. **Clone the repository**:

```bash
git clone <repo-url>
cd <repo-folder>
```

2. **Install dependencies**:

```bash
npm install
# or
yarn install
```

3. **Create `.env.local` file** with your Asgardeo app details:

```env
NEXT_PUBLIC_ASGARDEO_CLIENT_ID=<your_client_id>
NEXT_PUBLIC_ASGARDEO_TENANT_DOMAIN=<your_tenant_domain>
NEXT_PUBLIC_ASGARDEO_BASE_URL=https://api.asgardeo.io/t/<tenant_domain>/oauth2
NEXT_PUBLIC_REDIRECT_URI=http://localhost:3000/callback
```

4. **Start the development server**:

```bash
npm run dev
# or
yarn dev
```

---

## Authentication Flow

1. User clicks **Login** → redirected to Asgardeo login page.  
2. User enters credentials → receives an **ID token** and **access token**.  
3. Token is validated by the app → user gains access to protected pages.  
4. Logout clears tokens and session.  

---

## Usage

- **Login:** Click the login button → redirect to Asgardeo → login → return to dashboard.  
- **Protected Routes:** Only accessible after successful login.  
- **Logout:** Clears session and redirects to home page.  

---

## Notes

- Make sure your Asgardeo app **redirect URI** matches `NEXT_PUBLIC_REDIRECT_URI`.  
- For production, use HTTPS and secure cookies for token storage.  

---

## References

- [Asgardeo Docs](https://wso2.com/asgardeo)  
- [Next.js Documentation](https://nextjs.org/docs)  
- [OAuth2 / OpenID Connect](https://oauth.net/2/)  

---

## Author

Haritha — Next.js & Asgardeo Integration
