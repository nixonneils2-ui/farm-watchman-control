# Farm Watchman Control

Automated Farm Perimeter Control System - IoT Web Interface

## Overview

Farm Watchman is a modern, responsive web interface for controlling automated perimeter security systems on farms. It provides real-time status monitoring and system control through an intuitive power toggle interface.

## Features

- **Modern UI Design**: Dark theme with smooth animations and transitions
- **Real-time Status Display**: Visual status badge with active/standby indicators
- **Responsive Layout**: Works seamlessly on desktop, tablet, and mobile devices
- **System Logging**: Timestamped logs for all system state changes
- **Hardware Integration**: Ready for backend API integration with IoT devices (ESP32, Arduino, Raspberry Pi)

## Getting Started

1. Clone the repository
2. Open `index.html` in a web browser
3. Click the power button to toggle the system state

## Backend Integration

To connect this interface to your hardware backend:

1. Uncomment the fetch API calls in `index.html` (around lines 106-107)
2. Configure your backend endpoint (e.g., `/api/watchman`)
3. Implement state change logic on your hardware controller

Example:
```javascript
fetch('/api/watchman', {
  method: 'POST',
  headers: { 'Content-Type': 'application/json' },
  body: JSON.stringify({ state: isSystemOn ? 'ON' : 'OFF' })
});
```

## Project Structure

```
farm-watchman-control/
├── index.html          # Main interface
├── README.md          # Documentation
└── enhanced.html      # Enhanced version with improvements
```

## Browser Support

- Chrome/Chromium (latest)
- Firefox (latest)
- Safari (latest)
- Edge (latest)

## License

MIT License
