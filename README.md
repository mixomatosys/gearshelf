# GearShelf 🎸

**Simple audio plugin discovery and management tool. Built for real users, not over-engineered.**

## **What is GearShelf?**

GearShelf helps music producers discover new audio plugins and manage their existing plugin collections. It's designed to be simple, fast, and actually useful - not a showcase of complex technology.

## **🎯 Core Features**

### **Phase 1: Plugin Database & Web Interface** (In Development)
- Comprehensive database of 622+ audio plugins
- Advanced search by name, vendor, category, format (VST, VST3, AU, AAX)
- Multi-filter capabilities (price, OS, plugin type, etc.)
- Clean web interface with mobile support
- RESTful API for desktop app integration
- Internal network deployment on Proxmox LXC

### **Phase 2: Desktop Companion** (Planned)
- Scan your computer to inventory existing plugins
- Match local plugins to online database
- Personal plugin management and organization
- Cross-platform: Windows, macOS, Linux

### **Phase 3: Basic Sync** (Maybe Later)
- Optional user profiles for syncing across devices
- Plugin wishlist and favorites
- Basic preferences and settings

## **📋 Current Status**

🚧 **Phase 1 Development** - Plugin Database & Web Interface

- ✅ Project vision and documentation complete
- ✅ Technology stack selected (Node.js + PostgreSQL + nginx)
- ✅ Detailed Phase 1 plan established ([PHASE1_PLAN.md](PHASE1_PLAN.md))
- 🔄 Ready to start LXC container setup and implementation
- 📋 Target: Working internal plugin database in 2-3 weeks

## **🛠️ Technology Stack**

### **Phase 1: Web Database & API**
- **Infrastructure:** Proxmox LXC container (Ubuntu 22.04)
- **Backend:** Node.js + Express.js
- **Database:** PostgreSQL (scalable, supports future features)
- **Frontend:** Server-side rendered HTML + progressive JavaScript
- **Process Management:** systemd service
- **Reverse Proxy:** nginx (ready for external access)

### **Phase 2: Desktop App (Planned)**
- **Framework:** Electron (evolving from existing AudioShelf project)
- **API Integration:** REST calls to Phase 1 backend

## **📊 Plugin Database**

**Phase 1 Target: 1,500+ plugins** (expanding from 622 foundation)
- **Starting foundation:** 622 high-quality plugins from AudioShelf project
- **Major vendors:** Native Instruments, FabFilter, Waves, Xfer Records, Arturia, etc.
- **Categories:** Synthesizers, Effects, Samplers, Utilities, and more
- **Formats:** VST, VST3, AU, AAX with platform compatibility
- **Long-term goal:** Comprehensive database of 30,000+ available plugins

**Data expansion strategy includes:**
- Manual curation of top commercial plugins
- Admin tools for quality control and duplicate management  
- Automated data collection from major plugin sites
- Community submission system for comprehensive coverage
- Vendor partnerships for direct data integration

## **🚀 Getting Started**

**For Users:** Not ready yet! Check back soon.

**For Developers:**
```bash
# Clone the repository
git clone https://github.com/mixomatosys/gearshelf.git
cd gearshelf

# Check project status
cat DEVELOPMENT.md
```

## **📖 Documentation**

- [`PROJECT_VISION.md`](PROJECT_VISION.md) - Core principles and development philosophy
- [`PHASE1_PLAN.md`](PHASE1_PLAN.md) - Detailed Phase 1 implementation plan
- [`DATA_EXPANSION_STRATEGY.md`](DATA_EXPANSION_STRATEGY.md) - Strategy for scaling from 622 to 30,000+ plugins
- [`DEVELOPMENT.md`](DEVELOPMENT.md) - Development setup and contribution guidelines
- [`CHANGELOG.md`](CHANGELOG.md) - Version history and notable changes
- [`API.md`](API.md) - API documentation (when ready)

## **🤝 Contributing**

This project prioritizes **simplicity and user value** over technical complexity. 

**Before contributing:**
1. Read [`PROJECT_VISION.md`](PROJECT_VISION.md) to understand our philosophy
2. Check [`DEVELOPMENT.md`](DEVELOPMENT.md) for setup instructions
3. Focus on solving real user problems, not adding complex features

## **📝 License**

MIT License - see [`LICENSE`](LICENSE) file for details.

## **🔗 Links**

- **Repository:** https://github.com/mixomatosys/gearshelf
- **Issues:** https://github.com/mixomatosys/gearshelf/issues
- **Old Repository:** https://github.com/mixomatosys/gearshelf.io-old (previous over-engineered attempt)

---

**Built by music producers, for music producers. 🎵**