# Web Interface (Phase 1)

## **Goal**
Simple web interface for browsing and searching 622 audio plugins.

## **Success Criteria**
- ✅ Loads in <2 seconds
- ✅ Search by name, vendor, category
- ✅ Filter by format (VST/AU), price, OS
- ✅ Plugin detail pages
- ✅ Mobile responsive
- ✅ Works without JavaScript (progressive enhancement)

## **Technology Stack**
- **Backend:** Node.js + Express
- **Database:** SQLite (single file) OR JSON files (simpler)
- **Frontend:** HTML/CSS/JavaScript (no framework initially)
- **Deployment:** Single server + PM2/systemd

## **API Endpoints (Planned)**
```
GET /api/plugins              # List with search/filter
GET /api/plugins/:id          # Plugin details
GET /api/vendors              # Vendor list  
GET /api/categories           # Category hierarchy
GET /health                   # Health check
```

## **Current Status**
📋 **Planning Phase** - Documentation complete, ready to start implementation

## **Data Source**
- **Plugin Database:** 622 plugins from existing `audioshelf/data/plugin-metadata.json`
- **Migration Path:** JSON → SQLite for better querying (optional)

## **Next Steps**
1. Set up basic Express server
2. Create plugin data loading/serving
3. Build simple HTML interface with search
4. Add filtering and pagination
5. Style and make responsive