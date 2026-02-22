# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]

### Added
- Fresh project start with documentation-first approach
- Clear project vision and development guidelines
- Simple technology stack decisions (Node.js, SQLite, Electron)
- Plugin database foundation (622 plugins from AudioShelf project)

### Philosophy Changes
- Shifted from complex monorepo/microservices to simple single deployments
- Documentation-driven development before any coding
- Focus on core user value (plugin discovery) over advanced features
- Time-boxed phases (2-3 weeks each) instead of long-term planning

## [Previous Work - Archived]

### [gearshelf.io-old](https://github.com/mixomatosys/gearshelf.io-old) - Feb 21-22, 2026

**Lessons Learned:**
- ✅ Successfully created complete PostgreSQL database schema
- ✅ Built production-ready REST API with search/filtering
- ✅ Migrated 500 plugins with zero errors
- ❌ Over-engineered infrastructure (multi-container LXC deployment)
- ❌ Complex authentication system before proving user need
- ❌ 26-35 week timeline was unrealistic
- ❌ Infrastructure issues prevented shipping working product

**Key Achievements Worth Preserving:**
- Complete plugin data migration scripts
- Sophisticated API endpoint design
- Real plugin database with 500+ entries
- Relationships between plugins, vendors, categories

**What We're Not Repeating:**
- Complex container orchestration
- User authentication systems (until proven necessary)
- Community features before core functionality
- Multi-package monorepo structure
- Database containers and SSL certificate complexity

---

## Version History Philosophy

This changelog focuses on **user-visible changes** and **important technical decisions**, not every code commit.

### What Gets Documented:
- New features users can actually use
- Breaking API changes
- Important architectural decisions
- Deployment and setup changes
- Major bug fixes

### What Doesn't Get Documented:
- Internal refactoring (unless it affects performance)
- Development tooling updates
- Documentation typos and minor updates
- Work-in-progress commits