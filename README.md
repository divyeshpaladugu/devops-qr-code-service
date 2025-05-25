DEVOPS-QR-CODE-SERVICE
OVERVIEW
A full-stack QR code generation service using FastAPI (Python) and Next.js. Users submit a URL and the backend generates a PNG QR code, uploads it to S3, and returns the public link. The Next.js frontend allows instant preview and download.

FEATURES
On-demand QR code creation

S3 storage with public access

Dockerized backend and frontend

CI/CD pipeline via GitHub Actions to build and publish Docker images

PREREQUISITES
Node.js ≥16 & npm

Python 3.13 & pip

Docker Desktop

AWS credentials and region in a .env file

INSTALLATION
git clone https://github.com/divyeshpaladugu/devops-qr-code-service.git
cd devops-qr-code-service/api
pip install --pre -r requirements.txt
cd ../front-end-nextjs
npm install

USAGE
Backend:
cd api
uvicorn main:app --reload

Frontend:
cd ../front-end-nextjs
npm run dev
Open http://localhost:3000 to generate QR codes.

CI/CD
On every push to main, GitHub Actions builds Docker images for api and front-end-nextjs, tags them under divyeshpaladugu/, and pushes to Docker Hub.
