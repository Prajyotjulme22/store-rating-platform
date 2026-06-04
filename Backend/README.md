# Rating System Backend

## Setup Instructions

1. Install dependencies:
```bash
npm install
```

2. Configure PostgreSQL:
   - Install PostgreSQL if not already installed
   - Set postgres user password: `ALTER USER postgres PASSWORD 'postgres';`
   - Create database: `createdb -U postgres rating_system`

3. Configure environment variables in `.env`:
```
DB_HOST=localhost
DB_PORT=5432
DB_NAME=rating_system
DB_USER=postgres
DB_PASSWORD=postgres
JWT_SECRET=rating_system_jwt_secret_2024
```

4. Start the server:
```bash
npm run dev
```

5. Seed database with test data:
```bash
npm run seed:data
```

Or create only admin user:
```bash
npm run seed:admin
```

## API Endpoints

### Authentication
- POST `/api/auth/register` - User registration
- POST `/api/auth/login` - User login

### Admin Routes
- GET `/api/admin/dashboard` - Dashboard stats
- POST `/api/admin/users` - Create user
- POST `/api/admin/stores` - Create store
- GET `/api/admin/users` - List users with filters
- GET `/api/admin/stores` - List stores with ratings

### User Routes
- GET `/api/users/profile` - Get user profile
- PUT `/api/users/password` - Update password

### Store Routes
- GET `/api/stores` - List all stores (for normal users)
- GET `/api/stores/my-store` - Store owner dashboard

### Rating Routes
- POST `/api/ratings` - Submit/update rating
- GET `/api/ratings/my-ratings` - Get user's ratings

## Default Admin Credentials
- Email: admin@system.com
- Password: Admin@123