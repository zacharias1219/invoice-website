# **Invoice Marshall - Full Stack Invoice Platform**

**Invoice Marshall** is a robust full-stack invoice management system designed for businesses and freelancers to streamline invoicing processes. This platform enables seamless invoice creation, email notifications, and user authentication, all integrated with a user-friendly interface.

---

## **Features**

- **Custom Invoice Creation**:
  - Fully customizable invoice generation with real-time PDF creation using **jspdf**.
  - Automatically includes client details and payment terms.

- **Email Notifications**:
  - Sends invoices, payment reminders, and updates via **Mailtrap**.
  - Customizable email templates built with HTML and a no-code email builder.

- **User Authentication**:
  - Magic link authentication powered by **Auth.js**.
  - Secure user data storage and email verification.

- **Dashboard Analytics**:
  - Comprehensive dashboard with analytics for revenue, pending payments, and issued invoices.
  - Interactive charts built with **Shadcn UI**.

- **Responsive Design**:
  - Built with **Next.js 15** and styled using **TailwindCSS** for cross-device compatibility.

- **Database Integration**:
  - Data storage and retrieval using **PostgreSQL** with **Prisma ORM** for type-safe operations.

---

## **Tech Stack**

- **Frontend**: Next.js 15, TailwindCSS, Shadcn UI
- **Backend**: Prisma ORM, Neon PostgreSQL, Auth.js
- **Email Services**: Mailtrap, Nodemailer
- **PDF Creation**: jspdf
- **Deployment**: Vercel

---

## **Directory Structure**

```bash
├── app
│   ├── components
│   ├── pages
│   ├── styles
│   ├── services
├── prisma
│   └── schema.prisma
├── public
│   └── assets
├── utils
│   └── helpers
├── constants
├── README.md
└── package.json
```

---

## **Setup and Installation**

### **Prerequisites**

1. **Node.js**: Version 16 or above.
2. **Database**: PostgreSQL (Neon or equivalent).
3. **Mailtrap Account**: Register at [Mailtrap](https://mailtrap.io).
4. **Environment Variables**:
   - API keys for Mailtrap and Prisma.

### **Steps**

1. Clone the repository:

   ```bash
   git clone https://github.com/yourusername/invoice-marshall.git
   cd invoice-marshall
   ```

2. Install dependencies:

   ```bash
   npm install
   ```

3. Setup environment variables:
   - Create a `.env` file with the following:

     ```env
     DATABASE_URL=your_database_url
     MAILTRAP_USER=your_mailtrap_user
     MAILTRAP_PASS=your_mailtrap_pass
     AUTH_SECRET=your_auth_secret
     ```

4. Initialize Prisma:

   ```bash
   npx prisma generate
   npx prisma migrate dev
   ```

5. Run the development server:

   ```bash
   npm run dev
   ```

   Access the app at `http://localhost:3000`.

---

## **How It Works**

1. **User Authentication**:
   - Magic link authentication via Auth.js.
   - User data securely stored with hashed credentials.

2. **Invoice Management**:
   - Users can create, edit, and delete invoices.
   - Automatically generated PDFs and email notifications.

3. **Analytics Dashboard**:
   - Displays financial data and pending invoices.
   - Visualizes insights with animated charts.

---

## **Deployment**

1. **Build for Production**:

   ```bash
   npm run build
   ```

2. **Deploy**:
   - Host the app on Vercel or your preferred platform.
   - Update `.env` for production variables.

---

## **Future Enhancements**

- Add team collaboration features.
- Implement recurring invoices and reminders.
- Integrate with third-party accounting software.

---

## **Contributing**

Contributions are welcome! Fork the repository, create a feature branch, and submit a pull request.

---

## **License**

This project is licensed under the MIT License. See the `LICENSE` file for more details.

---
