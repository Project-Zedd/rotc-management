# ROTC Attendance System

A comprehensive military-themed attendance and cadet tracking system for Reserve Officers' Training Corps (ROTC) programs.

## 🎯 Overview

This system provides a complete solution for managing ROTC cadet attendance, ID cards, merit/demerit tracking, and study resources. Built with modern technologies and designed to support up to 3000 cadets.

## ✨ Features

### Core Features
- **QR Code Attendance**: Scan-based attendance tracking with geolocation
- **ID Card Generation**: Military-themed QR-coded ID cards
- **Multi-format Import**: Excel/Docx/PDF roster import
- **Google Forms Integration**: Automated cadet registration
- **Default Authentication**: Last name + birth year password system

### Advanced Features
- **Merit/Demerit System**: Point-based tracking with 10 categories
- **Badge & Ranking System**: 8 military-themed badges with 5-tier rankings
- **Study Resource Center**: File management with AWS S3 integration
- **Offline Mode**: Sync capabilities when reconnected
- **Mobile Responsive**: Works on all devices

### Admin Features
- **Dashboard Overview**: Real-time attendance statistics
- **Batch Operations**: Bulk ID card generation
- **Audit Logging**: Complete action tracking
- **2FA Authentication**: Enhanced security
- **Role Management**: Admin and super admin roles

### Cadet Features
- **Personal Dashboard**: Attendance history and statistics
- **Badge Display**: Earned badges and rankings
- **Resource Access**: Study materials and training files
- **Profile Management**: Update personal information

## 🛠 Technology Stack

### Backend
- **Node.js** with Express.js
- **PostgreSQL** database
- **Redis** for caching and sessions
- **AWS S3** for file storage
- **JWT** authentication

### Frontend
- **HTML5/CSS3/JavaScript**
- **Military-themed responsive design**
- **QR code scanning capabilities**
- **Mobile-first approach**

### Infrastructure
- **Docker** containerization
- **Docker Compose** for orchestration
- **Environment-based configuration**

## 🚀 Quick Start

### Prerequisites
- Node.js 16+
- PostgreSQL 12+
- Redis
- AWS S3 bucket (optional)

### Installation

1. **Clone the repository**
```bash
git clone [repository-url]
cd rotc-system
```

2. **Install dependencies**
```bash
cd backend
npm install
```

3. **Environment setup**
```bash
cp .env.example .env
# Edit .env with your configuration
```

4. **Database setup**
```bash
npm run migrate
npm run seed
```

5. **Start the application**
```bash
# Development
npm run dev

# Production
npm start
```

### Docker Deployment
```bash
docker-compose up -d
```

## 📊 Database Schema

### Core Tables
- `cadets` - Cadet information and profiles
- `attendance` - Attendance records and scans
- `merit_demerits` - Merit and demerit tracking
- `badges` - Badge definitions and criteria
- `resources` - Study materials and files
- `events` - Training events and schedules

### Key Relationships
- Cadets ↔ Attendance (one-to-many)
- Cadets ↔ Merit/Demerits (one-to-many)
- Cadets ↔ Badges (many-to-many)
- Events ↔ Attendance (one-to-many)

## 🔧 Configuration

### Environment Variables
```env
# Database
DATABASE_URL=postgresql://user:pass@localhost:5432/rotc_db

# Redis
REDIS_URL=redis://localhost:6379

# AWS
AWS_ACCESS_KEY_ID=your_key
AWS_SECRET_ACCESS_KEY=your_secret
AWS_REGION=us-east-1
AWS_S3_BUCKET=your_bucket

# JWT
JWT_SECRET=your_jwt_secret
JWT_REFRESH_SECRET=your_refresh_secret

# Email
SMTP_HOST=smtp.gmail.com
SMTP_PORT=587
SMTP_USER=your_email
SMTP_PASS=your_password
```

## 📱 Usage

### Admin Access
- **URL**: `http://localhost:5000/admin.html`
- **Default Login**: Configure in admin settings

### Cadet Access
- **URL**: `http://localhost:5000/cadet.html`
- **Login**: Student number + default password (last name + birth year)

### QR Code Scanning
- **Admin Scanner**: `http://localhost:5000/admin-scan.html`
- **Mobile Compatible**: Works on all devices

## 🎨 Military Theme

The system features a professional military design with:
- **Color Palette**: Military green, camouflage, and earth tones
- **Typography**: Bold, military-style fonts
- **Responsive Design**: Mobile-first approach
- **Accessibility**: WCAG 2.1 compliant

## 🔐 Security Features

- **JWT Authentication**: Secure token-based auth
- **2FA Support**: Two-factor authentication for admins
- **IP Whitelisting**: Restrict access by IP
- **Rate Limiting**: Prevent abuse
- **Input Validation**: SQL injection prevention
- **HTTPS Enforcement**: SSL/TLS encryption

## 📈 Performance

- **Scalability**: Supports 3000+ cadets
- **Caching**: Redis for improved performance
- **CDN**: AWS CloudFront for static assets
- **Database Indexing**: Optimized queries
- **Background Jobs**: Async processing

## 🧪 Testing

```bash
# Run tests
npm test

# Run with coverage
npm run test:coverage

# Load testing
npm run test:load
```

## 📚 API Documentation

Access the API documentation at:
- **Development**: `http://localhost:5000/api-docs`
- **Swagger UI**: Interactive API testing

## 🔄 Deployment

### Manual Deployment
1. Set up production environment variables
2. Run database migrations
3. Start with PM2: `pm2 start server.js`

### Docker Deployment
```bash
# Build and run
docker-compose up -d

# View logs
docker-compose logs -f
```

### Cloud Deployment
- **AWS ECS**: Container service
- **Heroku**: One-click deployment
- **DigitalOcean**: Droplet setup

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Add tests
5. Submit a pull request

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🆘 Support

For support, please contact:
- **Email**: support@rotc-system.com
- **Issues**: GitHub Issues
- **Documentation**: Wiki pages

## 🏆 Acknowledgments

- ROTC Command for requirements
- Development team for implementation
- Community for testing and feedback

---

**Built with ❤️ for ROTC programs worldwide**
