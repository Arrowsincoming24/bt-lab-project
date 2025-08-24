<<<<<<< HEAD
# Zenith National Bank - BT Lab Banking System

A comprehensive banking system built with Spring Boot backend and React TypeScript frontend, featuring Customer Management and Fixed Deposit (FD) Simulator modules.

## 🏦 Project Overview

This project implements a modern banking system with the following key features:

- **Customer Management**: Complete customer lifecycle management with KYC, classification, and communication
- **FD Simulator**: Advanced Fixed Deposit calculator with interest calculation engine
- **Multi-tier Architecture**: RESTful APIs with proper separation of concerns
- **Modern UI**: Beautiful, responsive interface with Zenith National Bank branding
- **Security**: JWT authentication, role-based access control, and audit trails

## 🎨 Brand Identity

**Zenith National Bank / Cashcached Brand Style Sheet**

### Colors
- **Primary Gradient**: #FF5BBE → #FF0099 (Pink to Magenta)
- **Secondary**: #7C3AED (Purple), #00F0FF (Aqua)
- **Neutrals**: #0D0D12 (Dark Background), #F5F5F7 (Light), #6B7280 (Grey)

### Typography
- **Primary Font**: Inter (Sans-serif)
- **Monospace**: Inter Mono (for financial data)
- **Weights**: Regular (400), Medium (500), Bold (700)

### Visual Style
- Modern, trustworthy, financial-tech focused
- Rounded corners (8px standard, 16px for buttons)
- Soft shadows and gradient highlights
- Dark background with gradient accents

## 🏗️ Architecture

### Backend (Spring Boot)
```
src/main/java/com/btlab/banking/
├── common/
│   ├── entity/BaseEntity.java
│   └── enums/
│       ├── Currency.java
│       └── Language.java
├── customer/
│   ├── entity/
│   │   ├── Customer.java
│   │   ├── CustomerAddress.java
│   │   ├── CustomerDocument.java
│   │   └── CustomerCommunication.java
│   └── enums/
│       ├── CustomerStatus.java
│       ├── CustomerTier.java
│       ├── Gender.java
│       ├── KycStatus.java
│       └── RiskProfile.java
├── fd/
│   ├── entity/
│   │   ├── FDProduct.java
│   │   ├── FDRateTier.java
│   │   ├── FDSimulation.java
│   │   ├── FDAccount.java
│   │   └── FDTransaction.java
│   └── enums/
│       ├── CompoundingFrequency.java
│       └── ProductStatus.java
└── BtLabBankingApplication.java
```

### Frontend (React TypeScript)
```
frontend/src/
├── components/
│   └── Layout/
│       ├── Layout.tsx
│       ├── Header.tsx
│       └── Sidebar.tsx
├── pages/
│   ├── Auth/
│   │   └── Login.tsx
│   ├── Dashboard/
│   │   └── Dashboard.tsx
│   ├── Customer/
│   │   ├── CustomerList.tsx
│   │   ├── CustomerDetail.tsx
│   │   └── CustomerCreate.tsx
│   └── FD/
│       ├── FDCalculator.tsx
│       ├── FDProducts.tsx
│       └── FDAccounts.tsx
├── hooks/
│   └── useAuth.ts
├── types/
│   └── index.ts
├── constants/
│   └── theme.ts
├── App.tsx
└── index.tsx
```

## 🚀 Getting Started

### Prerequisites
- Java 17 or higher
- Node.js 16 or higher
- MySQL 8.0 or higher
- Redis (for caching)

### Backend Setup

1. **Clone the repository**
   ```bash
   git clone <repository-url>
   cd bt-lab-project
   ```

2. **Configure Database**
   - Create MySQL database: `bt_lab_banking`
   - Update `application.yml` with your database credentials

3. **Run Spring Boot Application**
   ```bash
   ./mvnw spring-boot:run
   ```
   The backend will start on `http://localhost:8080`

### Frontend Setup

1. **Navigate to frontend directory**
   ```bash
   cd frontend
   ```

2. **Install dependencies**
   ```bash
   npm install
   ```

3. **Start development server**
   ```bash
   npm start
   ```
   The frontend will start on `http://localhost:3000`

## 🔐 Authentication

### Demo Credentials
- **Username**: `admin`
- **Password**: `admin123`

## 📊 Key Features

### Customer Module
- **Customer Classification**: Platinum, Gold, Silver, Bronze tiers
- **KYC Management**: Document verification and status tracking
- **Risk Assessment**: Conservative, Moderate, Aggressive profiles
- **Communication Log**: Track all customer interactions
- **360-Degree View**: Complete customer profile and history

### FD Simulator Module
- **Interest Calculation Engine**: Simple and compound interest
- **Multi-currency Support**: INR, KWD, JPY
- **Compounding Frequencies**: Daily, Monthly, Quarterly, Half-yearly, Annually
- **Rate Tiers**: Amount-based interest rate variations
- **Scenario Analysis**: Compare different FD options
- **Visual Analytics**: Charts and graphs for better understanding

### Technical Features
- **RESTful APIs**: Well-structured endpoints with proper HTTP methods
- **JWT Authentication**: Secure token-based authentication
- **Rate Limiting**: API protection against abuse
- **Audit Trail**: Complete audit logging for compliance
- **Multi-language Support**: English and Japanese
- **Real-time Processing**: Fast response times (<200ms customer lookup, <500ms FD simulation)

## 🛠️ Technology Stack

### Backend
- **Framework**: Spring Boot 3.x
- **Database**: MySQL 8.0
- **ORM**: JPA/Hibernate
- **Security**: Spring Security + JWT
- **Cache**: Redis
- **Documentation**: Swagger/OpenAPI
- **Build Tool**: Maven

### Frontend
- **Framework**: React 18 with TypeScript
- **UI Library**: Material-UI (MUI)
- **State Management**: React Query
- **Routing**: React Router DOM
- **Forms**: React Hook Form
- **Charts**: Recharts
- **Animations**: Framer Motion
- **Notifications**: React Hot Toast

## 📈 Performance Requirements

- **Response Times**: <200ms customer lookup, <500ms FD simulation
- **Concurrent Users**: 1000+ users
- **Uptime**: 99.9% availability
- **Database**: Optimized queries with proper indexing

## 🔒 Security Features

- **End-to-End Encryption**: All sensitive data encrypted
- **PCI DSS Compliance**: Payment card industry standards
- **Multi-Factor Authentication**: Enhanced security
- **Role-Based Access Control**: Granular permissions
- **Audit Logging**: Complete activity tracking
- **Input Validation**: Comprehensive data validation

## 📝 API Documentation

Once the backend is running, access the API documentation at:
- **Swagger UI**: `http://localhost:8080/api/swagger-ui.html`
- **OpenAPI JSON**: `http://localhost:8080/api/v3/api-docs`

## 🧪 Testing

### Backend Tests
```bash
./mvnw test
```

### Frontend Tests
```bash
cd frontend
npm test
```

## 📦 Deployment

### Backend Deployment
```bash
./mvnw clean package
java -jar target/bt-lab-banking-1.0.0.jar
```

### Frontend Deployment
```bash
cd frontend
npm run build
```

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Add tests for new functionality
5. Submit a pull request

## 📄 License

This project is licensed under the MIT License - see the LICENSE file for details.

## 🆘 Support

For support and questions:
- Create an issue in the repository
- Contact the development team
- Check the documentation

## 🗺️ Roadmap

- [ ] Advanced FD Calculator with visual charts
- [ ] Customer 360-degree view implementation
- [ ] Real-time notifications
- [ ] Mobile app development
- [ ] Advanced reporting and analytics
- [ ] Integration with external banking systems

---

**Zenith National Bank** - *Fixed Deposits, Reinvented* 🏦✨ 
=======
# bt-lab-project
bt-lab-project, react+springboot+typescript
>>>>>>> 3dd6f2c1cf99866c107218a507c0b4f1b5a748d7
