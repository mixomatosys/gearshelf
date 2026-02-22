# Desktop App (Phase 2)

## **Goal**
Cross-platform desktop app for managing local plugin inventory and discovering new plugins.

## **Success Criteria**
- ✅ Scans VST/VST3/AU plugins accurately on Windows, macOS, Linux
- ✅ Shows local plugin inventory in clean interface
- ✅ Integrates with web API for plugin discovery
- ✅ Matches local plugins to online database entries
- ✅ Basic plugin organization (favorites, categories)

## **Technology Stack**
- **Framework:** Electron (cross-platform, JavaScript ecosystem)
- **Base:** Evolution of existing AudioShelf project
- **Local Storage:** SQLite for user data
- **API Integration:** REST calls to web interface
- **UI:** HTML/CSS/JavaScript (consistent with web interface)

## **Core Features**

### **Plugin Scanning**
- Use existing AudioShelf scanner engine
- Platform-specific VST/AU folder detection
- Plugin metadata extraction (name, vendor, version)
- Duplicate detection and consolidation

### **Inventory Management**
- Local database of user's plugins
- Plugin status tracking (installed, favorites, hidden)
- Basic organization and categorization
- Export/import functionality

### **Discovery Integration**
- Browse online plugin database (from Phase 1)
- Search and filter plugins
- Mark plugins as "want to try" or "wishlist"
- Compare local inventory with online database

### **Smart Features**
- Automatic matching of local plugins to database entries
- Suggest similar plugins based on installed plugins
- Identify missing plugins from popular collections

## **Current Status**
📋 **Planned** - Waiting for Phase 1 (web interface) completion

## **Existing Assets**
- ✅ **AudioShelf scanner:** Working plugin detection engine
- ✅ **Plugin metadata:** 622 plugins already processed
- ✅ **Cross-platform:** Proven Windows/macOS/Linux support
- ✅ **Electron setup:** Basic app structure and UI

## **Migration Path**
1. **Extract scanner engine** from AudioShelf project
2. **Rebrand and simplify UI** (remove complex features)
3. **Add web API integration** for plugin discovery
4. **Implement basic cloud sync** (optional user profiles)

## **Next Steps**
1. Wait for Phase 1 web API completion
2. Extract and refactor AudioShelf scanner code
3. Build new simplified Electron interface
4. Integrate with web API for discovery features
5. Test on multiple platforms with real plugin installations