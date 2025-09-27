# AI Specialist Creation Guides

Complete guides for creating AI specialists from concept to implementation.

## Guide Structure

### 1. [Product Planning Guide](product-planning-guide.md)
**Start here** - Design your specialist before building it.

- Define specialist purpose and target users
- Plan memory architecture and content structure
- Design user experience and communication style
- Set success metrics and readiness checklist

### 2. [Technical Implementation Guide](technical-implementation-guide.md)
**Build your specialist** - Step-by-step implementation instructions.

- Two creation methods: Quick start vs GitHub creation
- Required file structure and configuration
- Auto-loaded files and critical setup
- Testing, troubleshooting, and maintenance

## Quick Start Workflow

1. **Plan** → Complete Product Planning Guide
2. **Build** → Follow Technical Implementation Guide
3. **Test** → Verify specialist works as designed
4. **Deploy** → Import to Magic Context platform
5. **Iterate** → Improve based on real usage

## Key Concepts

### Auto-Loaded Files (Critical)
These files are automatically shown by the platform:
- `/content/README.md` - User's first impression
- `/content/ai-instructions/getting_started.md` - AI's startup instructions

### Required Structure
```
your-specialist/
├── configuration/
│   └── module.json              # Specialist metadata
├── content/
│   ├── README.md               # Auto-loaded user guide
│   ├── ai-instructions/
│   │   ├── getting_started.md  # Auto-loaded AI instructions
│   │   └── core-instructions.md # Detailed AI programming
│   └── [domain folders]/       # Your specialist's content
└── protected-files/            # Optional private configs
```

## Success Criteria

After completing both guides, you should be able to:
- ✅ Create a working AI specialist from scratch
- ✅ Understand the platform's file structure requirements
- ✅ Design effective memory and content architecture
- ✅ Test and iterate on specialist behavior
- ✅ Deploy specialists that users can immediately use

## Need Help?

- Review the [FAQ](../reference/faq.md) for common questions
- Check [examples](../lessons/lesson-2-examples/) for inspiration
- Use the [templates](../templates/) as starting points

---

**Ready to create your first specialist?** Start with the [Product Planning Guide](product-planning-guide.md)!