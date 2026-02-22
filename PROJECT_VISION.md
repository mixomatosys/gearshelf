# GearShelf Project Vision & Guidelines

## **📋 Project Mission**

**Build the simplest possible tool that solves a real problem: helping music producers discover and manage their audio plugins.**

## **🎯 Core Principles (Hard Learned Lessons)**

### **1. Simplicity Over Sophistication**
- Start with the minimal viable solution
- Add complexity only when proven necessary  
- "Know when to stop" - resist over-engineering
- Ship working software over perfect architecture

### **2. User Value First**
- Focus on actual user problems, not technical curiosities
- Plugin discovery and management > community features
- Working desktop app > complex web platform
- Real plugin database > theoretical perfection

### **3. Documentation-Driven Development**
- **Always start with documentation** before coding
- Clear project vision and scope before implementation
- Readable code and clear architecture decisions
- Document lessons learned and pivots

### **4. Incremental & Iterative**
- Ship small, working pieces quickly
- Get user feedback early and often
- Build on proven foundations
- Each iteration should be deployable

## **🚫 What We're NOT Building (To Stay Focused)**

❌ **Complex user authentication systems** (unless users explicitly need them)  
❌ **Community features** (reviews, ratings, forums) - later phase  
❌ **Multi-container microservice architecture** - keep it simple  
❌ **Advanced admin interfaces** - focus on users, not admins  
❌ **Mobile apps** - desktop + web first  
❌ **AI/ML features** - solve basic problems first  

## **✅ What We ARE Building (Core Value)**

### **Phase 1: Plugin Discovery Database** (2-3 weeks)
✅ **Simple web interface** for browsing 500+ audio plugins  
✅ **Search and filtering** by category, vendor, format, price  
✅ **Plugin details** with descriptions, requirements, links  
✅ **Single-file deployment** (no complex infrastructure)

### **Phase 2: Desktop Companion App** (2-3 weeks) 
✅ **Local plugin scanner** (evolve from existing AudioShelf)  
✅ **Personal inventory management** (what plugins do I have?)  
✅ **Discovery integration** (browse online plugin database)  
✅ **Smart matching** (match local plugins to database entries)

### **Phase 3: Basic Cloud Sync** (1-2 weeks)
✅ **Simple user profiles** (optional, no social features)  
✅ **Plugin inventory backup** (sync across devices)  
✅ **Basic preferences** (favorite plugins, hide categories)

### **Later Phases** (Only if users ask for them):
- Community features (reviews, ratings)
- Mobile companion app
- Advanced integrations (DAW project scanning)
- Plugin recommendation engine

## **🛠️ Technology Choices (Keep It Simple)**

### **Backend:**
- **Node.js + Express** (simple, familiar)
- **SQLite database** (single file, no container complexity)
- **Direct deployment** on existing infrastructure
- **JSON for rapid prototyping** (can migrate to SQLite later)

### **Frontend Web:**
- **Static HTML/CSS/JS** or simple **Next.js** if needed
- **No complex state management** - keep it stateless
- **Mobile-responsive** but desktop-first

### **Desktop App:**
- **Electron** (cross-platform, JavaScript ecosystem)
- **Evolution from AudioShelf** (don't rebuild from scratch)
- **Local SQLite** for user data

### **Deployment:**
- **Single server deployment** (existing OpenClaw infrastructure)
- **PM2 or systemd** for process management
- **nginx reverse proxy** (simple, battle-tested)
- **Let's Encrypt SSL** (automated)

## **📊 Success Metrics**

### **Phase 1 Success:**
- Users can browse and search 500+ plugins effectively
- Clean, fast web interface that loads in <2 seconds
- Database deployable in <15 minutes

### **Phase 2 Success:**
- Desktop app scans user's plugins accurately
- Users can browse online database from desktop app
- Basic inventory management working

### **Phase 3 Success:**
- Users can sync their plugin inventory across devices
- Optional user profiles working without complexity

## **🔄 Development Process**

### **Before Writing Code:**
1. **Write documentation first** - README, API specs, user flows
2. **Define clear success criteria** for the feature/phase
3. **Time-box the work** (2-3 weeks max per phase)
4. **Plan the simplest possible implementation**

### **During Development:**
1. **Ship small, working pieces** weekly
2. **Test on real data** (use existing 622-plugin database)
3. **Document architectural decisions** as you go
4. **Push to GitHub daily** (never lose work)

### **After Each Phase:**
1. **Get real user feedback** (even if it's just Mixy testing)
2. **Document lessons learned** and pivot points
3. **Update project vision** if needed
4. **Plan next phase** based on actual usage

## **🚨 Warning Signs (When to Stop and Reassess)**

- Spending more than 1 week on infrastructure setup
- Adding features users haven't asked for
- Building "future-proof" abstractions before they're needed
- Debugging complex deployment issues instead of building features
- Choosing technologies you don't understand well

## **💪 Key Assets We're Building On**

✅ **622 audio plugins** with metadata (from AudioShelf)  
✅ **Working plugin scanner** (from AudioShelf)  
✅ **OpenClaw infrastructure** for hosting  
✅ **Lessons learned** about over-engineering  
✅ **Clear vision** of what users actually need  

---

**Bottom Line: Build the tool Mixy actually wants to use for managing plugins. Everything else is optional.**