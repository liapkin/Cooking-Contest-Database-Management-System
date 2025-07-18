# Cooking Contest Database Management System

## Project Overview

This is a comprehensive database management system for a cooking competition TV show, developed as a semester project for the Database course at NTUA (National Technical University of Athens) for Spring 2023-24.

## Key Features

### Database Schema
The system models a cooking competition where:
- **Chefs** compete in episodes organized by seasons
- **Judges** (who are also chefs) rate contestants' performances
- **Recipes** are assigned based on cuisines and themes
- **Nutritional information** and equipment usage are tracked

### Core Entities

#### Main Tables
- **Chefs** - Professional chef profiles with experience levels and specializations
- **Recipes** - Detailed cooking instructions with difficulty ratings
- **Episodes** - TV show episodes organized by seasons
- **Contests** - Chef participation records
- **Judges** - Judge assignments for episodes
- **Ratings** - Performance scores given by judges

#### Supporting Tables
- **National Cuisines** - Different cooking traditions
- **Ingredients** - Food items with nutritional data
- **Equipment** - Kitchen tools and appliances
- **Food Groups** - Ingredient categorization
- **Labels** - Recipe tags/categories
- **Themes** - Episode themes

### Business Rules

The system enforces several business rules through triggers:
- **Recency Rules**: Chefs cannot participate in more than 2 consecutive episodes (as contestant or judge)
- **Role Exclusivity**: A chef cannot be both contestant and judge in the same episode

### Analytical Queries

The project includes 15 complex analytical queries for various insights:
1. Average ratings per chef and cuisine
2. Chef participation by cuisine and season
3. Young chefs with most recipes
4. Chefs who never served as judges
5. Judge participation patterns
6. Popular recipe label combinations
7. Chef participation statistics
8. Equipment usage analysis
9. Nutritional analysis by season
10. Cuisine participation trends
11. Top-performing judges
12. Episode difficulty analysis
13. Professional training level analysis
14. Theme popularity
15. Unused food groups

## Project Structure

```
NTUA-DataBases-2024/
├── database/
│   ├── cooking_contest DDL.sql      # Complete database schema
│   ├── cooking_contest DML.sql      # Data manipulation procedures
│   ├── cooking_contest.sql          # Combined DDL and DML
│   └── ...                          # Various database versions
├── queries/
│   ├── 01.average_rate_per_chef_and_cuisine.sql
│   ├── 02.chefs_by_cuisine_and_season.sql
│   └── ...                          # 15 analytical queries
├── data/
│   ├── equipment.txt                # Equipment data
│   ├── theme.txt                    # Recipe themes
│   └── unit_converter.xlsx         # Unit conversions
├── images/
│   └── ER_Diagram.png              # Database schema visualization
└── README.md                        # This file
```

## Technical Details

### Database Features
- **Stored Procedures**: Automated data population for contests, judges, and ratings
- **Triggers**: Business rule enforcement
- **Views**: Simplified data access (chefs_view, knows, recipe_nut_info)
- **Indexes**: Performance optimization on key columns

### Key Stored Procedures
- `fill_contest()` - Populates contest participants
- `fill_judges()` - Assigns judges to episodes
- `fill_contest_cuisine()` - Assigns cuisines to contestants
- `fill_contest_recipe()` - Assigns recipes to contestants
- `fill_rating()` - Generates ratings

## Team Members
- Κωνσταντίνος Λιαπάκης,
- Νίκος Αλεξανδρόπουλος,
- Κωνσταντίνος Αλεξανδρόπουλος
 
## Course Information
- **Course**: Databases
- **Institution**: National Technical University of Athens (NTUA)
- **Semester**: Spring 2023-24
- **Department**: School of Electrical and Computer Engineering

## License
This is an educational project developed as part of coursework at NTUA.
