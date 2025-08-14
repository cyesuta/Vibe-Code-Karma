# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]

## [1.6.0] - 2025-08-14

### Added
- Comprehensive database selection guide (`database-choice.md`) with AI-assisted development perspective:
  - Quick comparison table for MySQL, MongoDB, PostgreSQL, SQLite at document top
  - AI security considerations and development efficiency criteria
  - Complete restructuring into logical sections: Relational Databases, NoSQL, Vector Databases
  - In-depth analysis of each database with pros/cons, use cases, and market competitors
  - New Vector Database section covering Pinecone, ChromaDB, Weaviate, Qdrant, Milvus
  - Personal developer selection recommendations for different project stages
  - Market competitor analysis for each database category

### Enhanced
- README.md navigation with new Database Choice Guide link under "資料庫、RAG" section
- Database guide structured with clear hierarchy: comparison table → selection criteria → database types → recommendations
- Each database section includes detailed technical analysis, performance characteristics, and practical applications
- Vector database coverage for modern AI application development needs

### Restructured
- Database content organized by database types rather than scattered analysis:
  - 🗄️ Relational Databases (MySQL, PostgreSQL, SQLite)
  - 📄 NoSQL Databases (MongoDB and competitors)  
  - 🧠 Vector Databases (AI-era specialized solutions)
  - 🎯 Personal Developer Recommendations
- Comparison table moved to top for quick decision-making reference
- Selection criteria clearly defined before diving into technical details

### Technical Coverage
- Complete analysis of ACID compliance, scalability, performance characteristics
- Market positioning and competitor landscape for each database type
- AI-assisted development considerations throughout the guide
- Modern application architecture patterns (hybrid storage strategies)
- Practical deployment scenarios from prototype to production

## [1.5.0] - 2025-08-14

### Added
- Comprehensive JavaScript animation libraries guide with major restructuring and optimization:
  - Complete reorganization into five clear categories: Universal Libraries, Framework Ecosystems, Traditional Solutions, Special Solutions, HTML5 Native
  - Detailed comparison table moved to top for quick reference
  - In-depth analysis of GSAP vs Anime.js performance and feature comparison
  - React ecosystem deep dive with city infrastructure analogy explanation
  - Vue and Svelte built-in animation systems coverage
  - Three.js vs GSAP dimensional differences analysis
  - HTML5 native animations vs JavaScript libraries performance comparison

### Enhanced
- README.md navigation with new JavaScript Animation Libraries Guide link
- Streamlined content structure by removing redundant sections:
  - Removed Technical Selection Guide section (consolidated into individual categories)
  - Removed Performance and Security Considerations section
  - Removed Academic Summary section to avoid content duplication
- All code examples removed to focus on conceptual understanding and selection guidance
- Five-tier classification system for better content organization

### Restructured
- Complete document reorganization following user specifications:
  - Comparison table positioned at document top
  - Content grouped by animation library categories rather than scattered topics
  - Each category contains relevant technical details, use cases, and selection criteria
  - Eliminated content redundancy while maintaining comprehensive coverage

### Educational Content
- Framework usage limitation explanations (why React libraries require React framework)
- Declarative vs imperative animation triggering mechanisms
- SSR framework integration concepts and challenges
- Modern web animation best practices and mixed-usage strategies
- Historical context: jQuery's evolution from pioneer to "retired legend"

### Technical Analysis
- Performance tier ratings: GSAP (S-Tier) vs React libraries (A-Tier) vs others
- Animation capability scope: DOM manipulation vs 3D world creation vs UI state management
- Integration complexity: universal libraries vs framework-specific solutions
- Cost considerations: commercial vs open-source solutions

## [1.4.0] - 2025-08-14

### Added
- New comprehensive JavaScript animation libraries comparison guide (`js-animation-libraries.md`)
- Deep dive into modern web animation ecosystem including:
  - Universal animation libraries: GSAP, Anime.js with detailed feature comparison
  - Framework-specific solutions: React (Framer Motion, React Spring), Vue Transitions, Svelte animations
  - Professional domain libraries: Three.js for 3D, Lottie for After Effects integration
  - Scroll-triggered animation libraries: ScrollMagic, ScrollReveal
  - HTML5 native animations vs JavaScript libraries performance analysis

### Enhanced
- Detailed React ecosystem explanation with city infrastructure analogy
- Frontend vs backend rendering concepts in animation context
- GSAP vs Three.js dimensional differences and use case clarification
- Performance comparison between CSS/WAAPI native animations and JavaScript libraries
- Technical limitations explanation for React ecosystem animation libraries

### Educational Content
- Framework animation capabilities: Vue built-in transitions, Svelte animation directives
- jQuery animation legacy status and modern alternatives explanation
- SSR framework animation integration best practices
- Complete feature comparison table with 11 animation solutions
- Practical selection guidelines based on project needs and tech stack

### Technical Analysis
- Why React ecosystem libraries require React framework usage
- Browser hardware acceleration and performance optimization insights
- Animation triggering mechanisms: imperative vs declarative approaches
- Cross-browser compatibility and modern web standards evolution

## [1.3.0] - 2025-08-14

### Added
- Comprehensive WebAssembly alternative solutions for frontend web development:
  - Canvas API, WebGL, CSS Filters for image processing
  - Web Workers, WebCodecs API for performance optimization
  - D3.js, Chart.js, Plotly.js, Observable Plot, Apache ECharts for data visualization
- Comprehensive WebAssembly alternative solutions for backend web development:
  - Image processing alternatives: Node.js+Sharp/Jimp, Python+Pillow/OpenCV, Go+imaging/gocv, Rust+image/photon, PHP+GD/ImageMagick
  - Data visualization solutions for various backend technologies

### Removed
- WebAssembly entry from blockchain development section
- Entire "區塊鏈與新興技術" (Blockchain and Emerging Technologies) section from programming language guide
- WebAssembly dependencies while preserving comprehensive alternative solutions

### Changed
- Enhanced programming language guide structure by replacing WebAssembly with practical, widely-supported alternatives
- Improved focus on mainstream technologies and proven solutions for web development

## [1.2.0] - 2025-01-13

### Added
- Icon-categorized lists for native development scenarios in programming language guide
- Mobile-friendly table structure for better readability

### Changed
- Removed blockquote formatting (>) from mobile development section for better GitHub visibility
- Merged language and platform columns in mobile development table
- Simplified table structure by removing pros/cons column
- Enhanced overall formatting and organization for mobile devices

### Improved
- Mobile readability across all sections
- Visual hierarchy with better use of icons and categorization

## [1.1.0] - 2025-01-13

### Added
- Comprehensive "What is Vibe Coding?" section to README
- Detailed Vibe Coding application scenarios with 4 main categories:
  - 🚀 Coding (programming language comparisons, web development)
  - 📝 Knowledge Management & Research
  - 🔍 Data Collection & Analysis
  - ⚙️ Daily Automation
  - 🎮 Creative & Experimental
- Practical examples and AI-assisted development perspective throughout content

### Changed
- Updated README with extensive content about Vibe Coding philosophy and applications
- Reorganized content structure with better categorization
- Updated copyright information to Cyesuta <cyesuta@gmail.com> in LICENSE
- Renamed `programming language.md` to `programming-language.md` for consistency

### Fixed
- Corrected link from `web-deployment-guide.html` to `web-deployment-guide.md`

### Removed
- Summary and market trends sections from programming language guide for better focus

## [1.0.0] - 2025-01-13

### Added
- Initial project setup with comprehensive README.md
- Complete programming language comparison guide covering:
  - Mobile development (native vs cross-platform)
  - Web development (frontend and backend)
  - Desktop development
  - System administration
  - Data science and AI
  - Blockchain and emerging technologies
- CSR vs Traditional HTML web development guide
- MIT License with proper attribution
- .gitignore file to exclude inappropriate content (old folder, system files)
- Project structure with clear navigation and links

### Features
- Vibe Coding compatibility assessments for each programming language
- AI-assisted development considerations
- Real-world application examples and use cases
- Modern development approach focusing on practical implementation

---

## Version History

- **v1.3.0**: WebAssembly alternatives implementation and blockchain section removal
- **v1.2.0**: Mobile readability improvements and table restructuring
- **v1.1.0**: Content expansion with Vibe Coding scenarios and copyright updates  
- **v1.0.0**: Initial release with comprehensive programming guides

## Contributing

Please read our [contributing guidelines](README.md#🤝-貢獻指南) before submitting changes.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.