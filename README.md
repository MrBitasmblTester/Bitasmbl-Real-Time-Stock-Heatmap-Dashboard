# Bitasmbl-Real-Time-Stock-Heatmap-Dashboard — Real-Time Stock Heatmap Dashboard

## Description

Build an interactive dashboard that visualizes live stock market performance using a color-coded heatmap. Users can filter sectors, view market movements, and monitor real-time changes as data updates dynamically.

## Tech Stack
- FastAPI (API)
- React (Front-End)
- Chart.js (Visualization)

## Requirements
- Fetch real-time and periodically updated stock market data
- Render an interactive heatmap representing stock performance
- Allow users to filter stocks by category, sector, or custom criteria
- Display trend changes with smooth, real-time UI updates
- Handle API rate limits, errors, or missing data gracefully

## Installation

Backend:
bash
# Clone the repository
git clone https://github.com/your-username/Bitasmbl-Real-Time-Stock-Heatmap-Dashboard.git
cd Bitasmbl-Real-Time-Stock-Heatmap-Dashboard
# Set up a virtual environment
python3 -m venv venv
source venv/bin/activate  # On Windows use "venv\\Scripts\\activate"
# Install dependencies
pip install fastapi uvicorn python-dotenv httpx


# Environment Variables
Create a `.env` file in the root directory:
ini
# API key for fetching stock data
STOCK_API_KEY=your_stock_api_key_here
# (Optional) API rate limit settings
API_RATE_LIMIT=your_rate_limit_value


Frontend:
bash
# Navigate to the frontend directory
cd frontend
# Install dependencies
npm install


## Usage

1. Start the backend server:
bash
uvicorn main:app --reload

2. In a separate terminal, start the frontend:
bash
cd frontend
npm start

3. Open your browser and visit `http://localhost:3000` to view the dashboard.

## Implementation Steps

1. Initialize a FastAPI project with folder structure and dependencies.
2. Create API endpoints to fetch and serve live stock data (`/api/stocks`).
3. Implement data fetching service in FastAPI using `httpx` and schedule periodic updates.
4. Handle API rate limits and errors gracefully within the service layer.
5. Initialize a React application using Create React App in the `frontend` folder.
6. Install and configure Chart.js for data visualization.
7. Build a heatmap component in React that consumes the `/api/stocks` endpoint.
8. Add filter controls for sectors, categories, and custom criteria.
9. Implement real-time UI updates using polling or WebSocket connections.
10. Add loading and error states to enhance user experience.

## API Endpoints

- GET /api/stocks?sector={sector}&category={category}
  Returns live and periodically updated stock performance data.
- GET /api/health
  Returns the health status of the API service.