# Shared Utilities

## **Purpose**
Common code, types, and utilities shared between web interface and desktop app.

## **Contents**

### **Types & Interfaces**
- Plugin data structures
- API request/response types  
- Configuration interfaces
- Common enums (PluginFormat, OperatingSystem, etc.)

### **Utilities**
- Plugin data validation
- Search/filter helpers
- File path utilities
- API client helpers

### **Constants**
- Plugin categories and subcategories
- Supported file extensions
- Default configuration values
- API endpoint URLs

## **Technology**
- **TypeScript** for type definitions
- **No framework dependencies** (pure JS/TS)
- **Node.js compatible** (works in both browser and Electron)

## **Current Status**
📋 **Placeholder** - Will be populated as web and desktop apps are built

## **Structure**
```
shared/
├── types/           # TypeScript type definitions
│   ├── plugin.ts    # Plugin-related types
│   ├── api.ts       # API request/response types  
│   └── config.ts    # Configuration types
├── utils/           # Shared utility functions
│   ├── validation.ts # Data validation helpers
│   ├── search.ts    # Search/filter utilities
│   └── files.ts     # File/path utilities
├── constants/       # Shared constants
│   ├── categories.ts # Plugin categories
│   ├── formats.ts   # Plugin format definitions
│   └── config.ts    # Default configurations
└── api/             # API client utilities
    └── client.ts    # HTTP client helpers
```