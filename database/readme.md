# Database Design & Data Modeling Guide

This folder contains your database design work and data modeling projects. Database skills are critical in GIS - proper database design ensures data integrity, performance, and scalability of spatial applications.

## What to Include

**Include database work that:**
- Demonstrates understanding of database design principles
- Shows spatial database knowledge (geodatabases, PostGIS, SpatiaLite)
- Represents well-designed, normalized schemas
- Solves real problems with appropriate data structures
- You can explain and defend design decisions

**You don't need to include:**
- Simple tutorial exercises
- Database designs you struggled with or didn't understand
- Work that doesn't reflect best practices
- Projects on topics you're not interested in

**Remember**: Quality database design shows deep understanding of data relationships and spatial data management - include work that demonstrates this expertise.

## Types of Database Work to Consider

### Database Design Projects
Complete database designs including:
- Entity-Relationship Diagrams (ERDs)
- Normalized table structures
- Relationship definitions and cardinality
- Primary and foreign key constraints
- Data validation rules and domains

### Geodatabase Designs
ArcGIS geodatabase projects featuring:
- Feature classes and tables
- Relationship classes
- Domains and subtypes
- Topology rules
- Network datasets or parcel fabrics

### Spatial Database Implementations
PostGIS, SpatiaLite, or other spatial database work:
- Spatial data types and geometry columns
- Spatial indexes for performance
- Complex spatial queries
- Integration with applications
- Database administration tasks

### Data Management Projects
Projects demonstrating:
- Database optimization and performance tuning
- Data migration and ETL processes
- Backup and recovery procedures
- Multi-user editing workflows
- Version management

### Schema Documentation
Well-documented database designs showing:
- Data dictionary with field definitions
- Relationship documentation
- Business rules and constraints
- Use cases and workflows
- Security and access considerations

## What Makes Strong Database Work?

### Proper Normalization
- Eliminate data redundancy
- Apply appropriate normal forms (1NF, 2NF, 3NF)
- Balance normalization with performance
- Document denormalization decisions

### Clear Relationships
- Well-defined primary and foreign keys
- Appropriate cardinality (one-to-one, one-to-many, many-to-many)
- Relationship classes in geodatabases
- Referential integrity constraints

### Data Integrity
- Proper data types for each field
- Domain constraints and validation rules
- Check constraints where appropriate
- Null handling strategies

### Spatial Considerations
- Appropriate spatial data types
- Spatial reference system documentation
- Spatial indexes for performance
- Topology rules for data quality

### Documentation
- Clear ERD diagrams
- Data dictionary
- Business rules
- Design decisions and rationale

## File Formats

### ERD Diagrams
Upload as images or PDFs:
- PNG or PDF format
- High resolution (readable when zoomed)
- Clear labels and notation
- Standard ERD symbols (crow's foot, UML, etc.)
- Store in main `images/` folder or as PDFs here

### Schema Documentation
Upload as PDFs:
- Complete data dictionaries
- Table and field descriptions
- Relationship documentation
- Business rules and constraints

### SQL Scripts (Optional)
Link to GitHub repositories containing:
- CREATE TABLE statements
- Index creation
- View definitions
- Sample queries

## Creating Your Landing Page

Use `database-projects.md` as your landing page that:
- Lists all database projects
- Shows ERD diagrams
- Describes design approach and decisions
- Links to documentation files
- Notes skills demonstrated
- Links to code repositories if applicable

## Documenting Database Projects

For each database project, include:

### Project Context
- What was the database designed for?
- Who are the users or stakeholders?
- What problems does it solve?
- Course or real-world application?

### Design Approach
- What normalization level did you apply?
- How did you handle spatial data?
- What design patterns did you use?
- Why did you make key decisions?

### ERD and Schema
- Include complete ERD diagram
- List main tables/feature classes
- Describe key relationships
- Note important constraints

### Implementation Details
- What platform (PostgreSQL/PostGIS, Geodatabase, SQLite)?
- Performance optimizations (indexes, partitioning)?
- Security considerations?
- Scalability approach?

### Skills Demonstrated
- Database normalization and design
- ERD creation and data modeling
- Spatial database implementation
- SQL and query optimization
- Data integrity and validation
- Database administration
- Performance tuning

## Tips for Success

### Design Quality
- **Follow best practices**: Apply normalization appropriately
- **Document decisions**: Explain why you designed it that way
- **Consider users**: Design for how data will be accessed and used
- **Plan for growth**: Consider scalability and future needs

### Visual Presentation
- **Clear ERDs**: Use standard notation, organize logically
- **Readable diagrams**: Ensure text is legible, entities are well-spaced
- **Professional tools**: Use proper ERD software (draw.io, Lucidchart, etc.)
- **Consistent notation**: Stick to one ERD style throughout

### Documentation
- **Complete data dictionary**: Define every table and field
- **Relationship documentation**: Explain all connections
- **Business rules**: Note validation and constraints
- **Examples**: Show sample data or use cases

### Before Sharing
- **Review for errors**: Check foreign key relationships, data types
- **Remove sensitive info**: Don't include actual production data
- **Verify diagrams**: Ensure ERDs match documentation
- **Test complexity**: Is it appropriately complex for the problem?

## Spatial Database Considerations

### Geodatabase Features
Document use of:
- Relationship classes
- Domains and coded value domains
- Subtypes
- Topology rules
- Network datasets
- Annotation and dimension classes

### PostGIS/SpatiaLite Features
Document use of:
- Spatial data types (geometry, geography)
- Spatial indexes (GIST, BRIN)
- Spatial functions and operators
- Complex spatial queries
- Performance optimization strategies

## How Much Database Work to Include?

**Starting out**: 1-2 well-designed database projects

**Recommended**: 2-4 projects showing:
- Different database platforms (geodatabase, PostGIS, etc.)
- Different complexity levels
- Different application areas
- Evolution of your skills

**Maximum**: 5 projects (focus on best work)

## Examples

### Strong Database Project Description

**Project Title**: Parks & Recreation Asset Management Database  
**Course**: GIS 1050 - Relational Database Management for GIS  
**Date**: October 2024  
**Platform**: ArcGIS Pro Enterprise Geodatabase (PostgreSQL backend)

**Overview**: Designed a comprehensive database for managing city parks assets including facilities, equipment, maintenance schedules, and inspection records. The database supports multi-user editing, tracks maintenance history, and integrates with mobile data collection workflows for field inspections.

**Database Design**:
The database follows third normal form (3NF) to eliminate redundancy while maintaining spatial relationships. Key design decisions include using subtypes for different park facility types and relationship classes to link inspection records to specific assets.

**Key Features**:
- Normalized to 3NF with appropriate denormalization for spatial queries
- 12 feature classes and 8 tables
- 15 relationship classes enforcing referential integrity
- Domains for standardized data entry (facility type, condition ratings, etc.)
- Topology rules ensuring spatial data quality
- Automated maintenance scheduling through database triggers

**Entity-Relationship Diagram**:
![ERD Diagram](../images/parks-database-erd.png)

**Schema Components**:

**Feature Classes**:
- Parks - Polygon feature class with park boundaries and attributes
- Facilities - Point feature class for buildings, playgrounds, etc. (with subtypes)
- Trails - Polyline feature class with surface type and difficulty ratings
- Maintenance_Zones - Polygon feature class for crew assignment areas

**Tables**:
- Inspections - Links to facilities through relationship class
- Work_Orders - Maintenance tasks and scheduling
- Equipment - Assets assigned to specific facilities
- Maintenance_History - Complete audit trail of all maintenance activities

**Relationships**:
- Parks to Facilities (1:M) - Each park contains multiple facilities
- Facilities to Inspections (1:M) - Track inspection history for each facility
- Facilities to Equipment (1:M) - Equipment inventory by location
- Work_Orders to Facilities (M:M through junction table) - Single work order can affect multiple facilities

**Constraints & Validation**:
- Primary keys: GlobalID on all feature classes
- Foreign keys: Enforce referential integrity across relationships
- Domains: Facility_Type (playground, restroom, pavilion, etc.), Condition_Rating (1-5 scale), Surface_Type
- Check constraints: Inspection dates cannot be in future, equipment purchase dates must precede installation dates

**Skills Demonstrated**:
- Database normalization (1NF, 2NF, 3NF)
- ERD creation using crow's foot notation
- Enterprise geodatabase design
- Relationship class implementation
- Domain and subtype configuration
- Topology rule definition
- Multi-user editing workflow design
- Data integrity and validation strategies
- Performance optimization through spatial indexing

**Technical Implementation**:
Implemented in ArcGIS Pro using PostgreSQL backend for enterprise deployment. Applied spatial indexes on all geometry fields. Configured archiving for audit trail. Set up version management for multi-user editing workflows. Database supports 15 concurrent editors with sub-second query performance.

**[Download Full Schema Documentation (PDF)](parks-database-schema.pdf)** | **[View SQL Scripts (GitHub)](https://github.com/username/parks-database)**

### What to Avoid

**Weak description:**
"Database project for GIS class. Made some tables."

**Why it's weak**: No detail about design decisions, relationships, or complexity. Doesn't demonstrate understanding of database principles or spatial data management.

---

## Additional Resources

### ERD Tools
- [draw.io](https://www.drawio.com/) - Free, web-based diagramming
- [Lucidchart](https://www.lucidchart.com/) - Professional diagramming tool
- [dbdiagram.io](https://dbdiagram.io/) - Database diagram tool with code

### Database Documentation
- Data dictionary templates
- Schema documentation standards
- ERD notation guides (crow's foot, UML, Chen)

### Learning Resources
- Database normalization tutorials
- Spatial database best practices
- Geodatabase design patterns
- PostGIS documentation

---

[Back to Main README](../README.md)
