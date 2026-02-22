# Development Guide

## **🎯 Development Philosophy**

**Documentation First, Code Second**
- Always write docs before implementation
- Clear requirements and success criteria upfront
- Time-box features (2-3 weeks max per phase)

**Simple Tools, Proven Solutions**
- Use technologies you understand well
- Avoid "future-proofing" until you need it
- Ship working software over perfect architecture

## **⚠️ What We Learned (Don't Repeat These Mistakes)**

### **❌ Over-Engineering Trap**
- Previous attempt: 26-35 week plan with microservices, complex containers, user auth
- Result: Infrastructure issues, deployment problems, no shipped product
- **Lesson:** Start simple, add complexity only when proven necessary

### **❌ Infrastructure First**
- Previous attempt: PostgreSQL containers, nginx proxy, SSL certificates before MVP
- Result: Spending weeks on deployment instead of user features
- **Lesson:** Build core features first, optimize deployment later

### **❌ Feature Creep**
- Previous attempt: Community features, reviews, advanced admin interfaces
- Result: Lost focus on core problem (plugin discovery)
- **Lesson:** Focus on one problem, solve it well

## **✅ Current Approach**

### **Phase 1: Web Plugin Browser (2-3 weeks)**
**Goal:** Users can browse and search 622 plugins effectively

**Success Criteria:**
- Web interface loads in <2 seconds
- Search works for plugin names, vendors, categories
- Filtering works for format (VST/AU), price (free/paid), OS
- Plugin detail pages show useful information
- Deployable in <15 minutes

**Technology Choices:**
- **Backend:** Node.js + Express (familiar, fast to develop)
- **Database:** SQLite (single file, no container complexity) OR JSON files (even simpler)
- **Frontend:** Static HTML/CSS/JS (no framework complexity initially)

### **Phase 2: Desktop App (2-3 weeks)**
**Goal:** Users can manage their local plugin inventory

**Success Criteria:**
- Scans user's VST/AU plugins accurately
- Shows local plugin inventory in clean interface
- Can browse online plugin database from desktop
- Basic matching of local plugins to database entries

**Technology Choices:**
- **Framework:** Electron (evolve existing AudioShelf project)
- **Local Storage:** SQLite for user data
- **API Integration:** REST calls to Phase 1 web API

## **🛠️ Development Setup**

### **Prerequisites**
- Node.js 18+ (LTS)
- Git
- SQLite (if using database approach)

### **Initial Setup**
```bash
# Clone and setup
git clone https://github.com/mixomatosys/gearshelf.git
cd gearshelf

# Install dependencies (when package.json exists)
npm install

# Copy example environment file
cp .env.example .env

# Setup database (approach TBD)
# npm run setup-db
```

### **Development Workflow**

1. **Before Starting Any Feature:**
   - Update this file with clear requirements
   - Define success criteria
   - Time-box the work (max 1-2 weeks)
   - Write API spec or interface contracts

2. **During Development:**
   - Commit and push daily (never lose work)
   - Write tests for core functionality
   - Update documentation as you go
   - Keep it simple - resist complexity

3. **Before Shipping:**
   - Test on real data (use existing 622-plugin dataset)
   - Verify deployment process works
   - Update CHANGELOG.md
   - Tag release with semantic versioning

## **📊 Data Sources**

### **Plugin Database**
- **Source:** Existing `audioshelf/data/plugin-metadata.json` (622 plugins)
- **Quality:** Curated data with names, vendors, categories, descriptions
- **Vendors:** Major plugin manufacturers (Native Instruments, FabFilter, etc.)
- **Categories:** Synthesizers, Effects, Samplers, etc.

### **Local Plugin Scanning**
- **Source:** Existing AudioShelf scanner engine
- **Capabilities:** VST, VST3, AU plugin detection
- **Platforms:** Windows, macOS, Linux
- **Status:** Working code available for integration

## **🚀 Deployment Strategy**

### **Phase 1: Simple Deployment**
- **Target:** Single VPS or existing OpenClaw infrastructure
- **Process Manager:** PM2 or systemd service
- **Reverse Proxy:** nginx (simple configuration)
- **Database:** SQLite file or JSON (easy backup/restore)
- **SSL:** Let's Encrypt (automated renewal)

### **Phase 2: Desktop Distribution**
- **Packaging:** Electron Builder
- **Platforms:** Windows, macOS, Linux
- **Updates:** Simple download from GitHub releases
- **Auto-update:** Only if users request it

## **🧪 Testing Strategy**

### **Backend Testing**
- **API Tests:** Jest + Supertest for endpoint testing
- **Database Tests:** In-memory SQLite for fast tests
- **Integration Tests:** Real plugin data validation

### **Desktop App Testing**
- **Unit Tests:** Core plugin scanning logic
- **Integration Tests:** API communication
- **Manual Testing:** Real plugin installations on each platform

### **Performance Testing**
- **Web Interface:** <2 second load times
- **API Responses:** <500ms for search queries
- **Desktop Scanning:** <30 seconds for typical plugin folder

## **📋 Code Standards**

### **Keep It Simple**
- Prefer readable code over clever code
- Use TypeScript for better developer experience
- ESLint + Prettier for consistent formatting
- Clear variable names and function purposes

### **Error Handling**
- Graceful degradation (web interface works without JavaScript)
- Clear error messages for users
- Proper logging for debugging
- Don't crash on missing data

### **Documentation**
- JSDoc comments for public APIs
- README files in each major directory
- API documentation with examples
- Deployment instructions that actually work

## **🚨 Warning Signs**

**Stop and reassess if:**
- Spending >1 week on infrastructure/deployment
- Adding features users haven't asked for
- Choosing technologies you don't understand
- Building "future-proof" abstractions prematurely
- Debugging complex problems instead of shipping features

## **📂 Project Structure**

```
gearshelf/
├── docs/                   # Project documentation
├── web/                    # Phase 1: Web interface
│   ├── src/               #   Source code
│   ├── data/              #   Plugin database
│   └── public/            #   Static assets
├── desktop/               # Phase 2: Electron app
│   ├── src/               #   App source code
│   ├── scanner/           #   Plugin scanning engine
│   └── assets/            #   App assets
├── shared/                # Shared utilities/types
├── scripts/               # Build and deployment scripts
└── tests/                 # Integration tests
```

## **🤝 Contributing**

### **Pull Request Process**
1. Fork the repository
2. Create feature branch (`git checkout -b feature-name`)
3. Write code following these guidelines
4. Test thoroughly on real plugin data
5. Update documentation
6. Submit PR with clear description of changes

### **Issue Reporting**
- Use GitHub Issues for bugs and feature requests
- Provide clear reproduction steps
- Include environment details (OS, Node version, etc.)
- Focus on user impact, not technical details

---

**Remember: We're building a useful tool, not a technology showcase. Keep it simple, ship it working.**