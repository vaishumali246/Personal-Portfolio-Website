# Vaishnavi Mali - Personal Portfolio Web Application
## Complete Consolidated Project Source Code
> Generated: 2026-10-06 14:01:44
> Stack: Java 21 / 25, Spring Boot 3.5, Spring Data JPA, Hibernate, Spring Security, Thymeleaf, MySQL 8 / MariaDB

---

## Table of Contents

### 1. Build & Database Configuration
- [`portfolio-app/pom.xml`](#portfolio-app-pomxml)
- [`portfolio-app/database-setup.sql`](#portfolio-app-database-setupsql)
- [`portfolio-app/src/main/resources/application.properties`](#portfolio-app-src-main-resources-applicationproperties)
- [`portfolio-app/src/main/resources/application-demo.properties`](#portfolio-app-src-main-resources-application-demoproperties)
- [`start-portfolio.bat`](#start-portfoliobat)
- [`stop-portfolio.bat`](#stop-portfoliobat)

### 2. Main Application & Framework Config
- [`portfolio-app/src/main/java/com/portfolio/PortfolioApplication.java`](#portfolio-app-src-main-java-com-portfolio-portfolioapplicationjava)
- [`portfolio-app/src/main/java/com/portfolio/config/SecurityConfig.java`](#portfolio-app-src-main-java-com-portfolio-config-securityconfigjava)
- [`portfolio-app/src/main/java/com/portfolio/config/WebConfig.java`](#portfolio-app-src-main-java-com-portfolio-config-webconfigjava)
- [`portfolio-app/src/main/java/com/portfolio/config/GlobalModelAttributes.java`](#portfolio-app-src-main-java-com-portfolio-config-globalmodelattributesjava)
- [`portfolio-app/src/main/java/com/portfolio/config/PortfolioProfileData.java`](#portfolio-app-src-main-java-com-portfolio-config-portfolioprofiledatajava)

### 3. Domain Entities & Enums
- [`portfolio-app/src/main/java/com/portfolio/entity/Achievement.java`](#portfolio-app-src-main-java-com-portfolio-entity-achievementjava)
- [`portfolio-app/src/main/java/com/portfolio/entity/AdminUser.java`](#portfolio-app-src-main-java-com-portfolio-entity-adminuserjava)
- [`portfolio-app/src/main/java/com/portfolio/entity/Certification.java`](#portfolio-app-src-main-java-com-portfolio-entity-certificationjava)
- [`portfolio-app/src/main/java/com/portfolio/entity/ContactMessage.java`](#portfolio-app-src-main-java-com-portfolio-entity-contactmessagejava)
- [`portfolio-app/src/main/java/com/portfolio/entity/Education.java`](#portfolio-app-src-main-java-com-portfolio-entity-educationjava)
- [`portfolio-app/src/main/java/com/portfolio/entity/Experience.java`](#portfolio-app-src-main-java-com-portfolio-entity-experiencejava)
- [`portfolio-app/src/main/java/com/portfolio/entity/Project.java`](#portfolio-app-src-main-java-com-portfolio-entity-projectjava)
- [`portfolio-app/src/main/java/com/portfolio/entity/ProjectCategory.java`](#portfolio-app-src-main-java-com-portfolio-entity-projectcategoryjava)
- [`portfolio-app/src/main/java/com/portfolio/entity/SettingKey.java`](#portfolio-app-src-main-java-com-portfolio-entity-settingkeyjava)
- [`portfolio-app/src/main/java/com/portfolio/entity/SiteSetting.java`](#portfolio-app-src-main-java-com-portfolio-entity-sitesettingjava)
- [`portfolio-app/src/main/java/com/portfolio/entity/Skill.java`](#portfolio-app-src-main-java-com-portfolio-entity-skilljava)

### 4. Data Transfer Objects (DTOs)
- [`portfolio-app/src/main/java/com/portfolio/dto/ChangePasswordForm.java`](#portfolio-app-src-main-java-com-portfolio-dto-changepasswordformjava)
- [`portfolio-app/src/main/java/com/portfolio/dto/DashboardStats.java`](#portfolio-app-src-main-java-com-portfolio-dto-dashboardstatsjava)
- [`portfolio-app/src/main/java/com/portfolio/dto/RegisterForm.java`](#portfolio-app-src-main-java-com-portfolio-dto-registerformjava)
- [`portfolio-app/src/main/java/com/portfolio/dto/ServiceItem.java`](#portfolio-app-src-main-java-com-portfolio-dto-serviceitemjava)

### 5. Spring Data JPA Repositories
- [`portfolio-app/src/main/java/com/portfolio/repository/AchievementRepository.java`](#portfolio-app-src-main-java-com-portfolio-repository-achievementrepositoryjava)
- [`portfolio-app/src/main/java/com/portfolio/repository/AdminUserRepository.java`](#portfolio-app-src-main-java-com-portfolio-repository-adminuserrepositoryjava)
- [`portfolio-app/src/main/java/com/portfolio/repository/CertificationRepository.java`](#portfolio-app-src-main-java-com-portfolio-repository-certificationrepositoryjava)
- [`portfolio-app/src/main/java/com/portfolio/repository/ContactMessageRepository.java`](#portfolio-app-src-main-java-com-portfolio-repository-contactmessagerepositoryjava)
- [`portfolio-app/src/main/java/com/portfolio/repository/EducationRepository.java`](#portfolio-app-src-main-java-com-portfolio-repository-educationrepositoryjava)
- [`portfolio-app/src/main/java/com/portfolio/repository/ExperienceRepository.java`](#portfolio-app-src-main-java-com-portfolio-repository-experiencerepositoryjava)
- [`portfolio-app/src/main/java/com/portfolio/repository/ProjectRepository.java`](#portfolio-app-src-main-java-com-portfolio-repository-projectrepositoryjava)
- [`portfolio-app/src/main/java/com/portfolio/repository/SiteSettingRepository.java`](#portfolio-app-src-main-java-com-portfolio-repository-sitesettingrepositoryjava)
- [`portfolio-app/src/main/java/com/portfolio/repository/SkillRepository.java`](#portfolio-app-src-main-java-com-portfolio-repository-skillrepositoryjava)

### 6. Service Layer (Interfaces & Implementations)
- [`portfolio-app/src/main/java/com/portfolio/service/AchievementService.java`](#portfolio-app-src-main-java-com-portfolio-service-achievementservicejava)
- [`portfolio-app/src/main/java/com/portfolio/service/CertificationService.java`](#portfolio-app-src-main-java-com-portfolio-service-certificationservicejava)
- [`portfolio-app/src/main/java/com/portfolio/service/ContactMessageService.java`](#portfolio-app-src-main-java-com-portfolio-service-contactmessageservicejava)
- [`portfolio-app/src/main/java/com/portfolio/service/ContactMessageServiceImpl.java`](#portfolio-app-src-main-java-com-portfolio-service-contactmessageserviceimpljava)
- [`portfolio-app/src/main/java/com/portfolio/service/DashboardService.java`](#portfolio-app-src-main-java-com-portfolio-service-dashboardservicejava)
- [`portfolio-app/src/main/java/com/portfolio/service/EducationService.java`](#portfolio-app-src-main-java-com-portfolio-service-educationservicejava)
- [`portfolio-app/src/main/java/com/portfolio/service/ExperienceService.java`](#portfolio-app-src-main-java-com-portfolio-service-experienceservicejava)
- [`portfolio-app/src/main/java/com/portfolio/service/FileStorageService.java`](#portfolio-app-src-main-java-com-portfolio-service-filestorageservicejava)
- [`portfolio-app/src/main/java/com/portfolio/service/ProjectService.java`](#portfolio-app-src-main-java-com-portfolio-service-projectservicejava)
- [`portfolio-app/src/main/java/com/portfolio/service/ProjectServiceImpl.java`](#portfolio-app-src-main-java-com-portfolio-service-projectserviceimpljava)
- [`portfolio-app/src/main/java/com/portfolio/service/SiteSettingService.java`](#portfolio-app-src-main-java-com-portfolio-service-sitesettingservicejava)
- [`portfolio-app/src/main/java/com/portfolio/service/SkillService.java`](#portfolio-app-src-main-java-com-portfolio-service-skillservicejava)
- [`portfolio-app/src/main/java/com/portfolio/service/SkillServiceImpl.java`](#portfolio-app-src-main-java-com-portfolio-service-skillserviceimpljava)
- [`portfolio-app/src/main/java/com/portfolio/service/UserService.java`](#portfolio-app-src-main-java-com-portfolio-service-userservicejava)

### 7. Security & Authentication Services
- [`portfolio-app/src/main/java/com/portfolio/security/AuthHelper.java`](#portfolio-app-src-main-java-com-portfolio-security-authhelperjava)
- [`portfolio-app/src/main/java/com/portfolio/security/CustomUserDetailsService.java`](#portfolio-app-src-main-java-com-portfolio-security-customuserdetailsservicejava)

### 8. Database Initialization & Exception Handling
- [`portfolio-app/src/main/java/com/portfolio/init/DataSeeder.java`](#portfolio-app-src-main-java-com-portfolio-init-dataseederjava)
- [`portfolio-app/src/main/java/com/portfolio/exception/GlobalExceptionHandler.java`](#portfolio-app-src-main-java-com-portfolio-exception-globalexceptionhandlerjava)
- [`portfolio-app/src/main/java/com/portfolio/exception/ResourceNotFoundException.java`](#portfolio-app-src-main-java-com-portfolio-exception-resourcenotfoundexceptionjava)

### 9. Public & Auth Web Controllers
- [`portfolio-app/src/main/java/com/portfolio/controller/PublicController.java`](#portfolio-app-src-main-java-com-portfolio-controller-publiccontrollerjava)
- [`portfolio-app/src/main/java/com/portfolio/controller/AuthController.java`](#portfolio-app-src-main-java-com-portfolio-controller-authcontrollerjava)
- [`portfolio-app/src/main/java/com/portfolio/controller/ExploreController.java`](#portfolio-app-src-main-java-com-portfolio-controller-explorecontrollerjava)
- [`portfolio-app/src/main/java/com/portfolio/controller/ResumeController.java`](#portfolio-app-src-main-java-com-portfolio-controller-resumecontrollerjava)
- [`portfolio-app/src/main/java/com/portfolio/controller/UserPortfolioController.java`](#portfolio-app-src-main-java-com-portfolio-controller-userportfoliocontrollerjava)

### 10. Admin Web Controllers
- [`portfolio-app/src/main/java/com/portfolio/controller/admin/AdminAchievementController.java`](#portfolio-app-src-main-java-com-portfolio-controller-admin-adminachievementcontrollerjava)
- [`portfolio-app/src/main/java/com/portfolio/controller/admin/AdminCertificationController.java`](#portfolio-app-src-main-java-com-portfolio-controller-admin-admincertificationcontrollerjava)
- [`portfolio-app/src/main/java/com/portfolio/controller/admin/AdminDashboardController.java`](#portfolio-app-src-main-java-com-portfolio-controller-admin-admindashboardcontrollerjava)
- [`portfolio-app/src/main/java/com/portfolio/controller/admin/AdminEducationController.java`](#portfolio-app-src-main-java-com-portfolio-controller-admin-admineducationcontrollerjava)
- [`portfolio-app/src/main/java/com/portfolio/controller/admin/AdminExperienceController.java`](#portfolio-app-src-main-java-com-portfolio-controller-admin-adminexperiencecontrollerjava)
- [`portfolio-app/src/main/java/com/portfolio/controller/admin/AdminLoginController.java`](#portfolio-app-src-main-java-com-portfolio-controller-admin-adminlogincontrollerjava)
- [`portfolio-app/src/main/java/com/portfolio/controller/admin/AdminMessageController.java`](#portfolio-app-src-main-java-com-portfolio-controller-admin-adminmessagecontrollerjava)
- [`portfolio-app/src/main/java/com/portfolio/controller/admin/AdminProjectController.java`](#portfolio-app-src-main-java-com-portfolio-controller-admin-adminprojectcontrollerjava)
- [`portfolio-app/src/main/java/com/portfolio/controller/admin/AdminSettingsController.java`](#portfolio-app-src-main-java-com-portfolio-controller-admin-adminsettingscontrollerjava)
- [`portfolio-app/src/main/java/com/portfolio/controller/admin/AdminSkillController.java`](#portfolio-app-src-main-java-com-portfolio-controller-admin-adminskillcontrollerjava)

### 11. Frontend Layout & Reusable Fragments
- [`portfolio-app/src/main/resources/templates/fragments/admin-sidebar.html`](#portfolio-app-src-main-resources-templates-fragments-admin-sidebarhtml)
- [`portfolio-app/src/main/resources/templates/fragments/admin-topbar.html`](#portfolio-app-src-main-resources-templates-fragments-admin-topbarhtml)
- [`portfolio-app/src/main/resources/templates/fragments/alerts.html`](#portfolio-app-src-main-resources-templates-fragments-alertshtml)
- [`portfolio-app/src/main/resources/templates/fragments/footer.html`](#portfolio-app-src-main-resources-templates-fragments-footerhtml)
- [`portfolio-app/src/main/resources/templates/fragments/head.html`](#portfolio-app-src-main-resources-templates-fragments-headhtml)
- [`portfolio-app/src/main/resources/templates/fragments/navbar.html`](#portfolio-app-src-main-resources-templates-fragments-navbarhtml)
- [`portfolio-app/src/main/resources/templates/fragments/scripts.html`](#portfolio-app-src-main-resources-templates-fragments-scriptshtml)

### 12. Public Website Templates
- [`portfolio-app/src/main/resources/templates/public/about.html`](#portfolio-app-src-main-resources-templates-public-abouthtml)
- [`portfolio-app/src/main/resources/templates/public/achievements.html`](#portfolio-app-src-main-resources-templates-public-achievementshtml)
- [`portfolio-app/src/main/resources/templates/public/certifications.html`](#portfolio-app-src-main-resources-templates-public-certificationshtml)
- [`portfolio-app/src/main/resources/templates/public/contact.html`](#portfolio-app-src-main-resources-templates-public-contacthtml)
- [`portfolio-app/src/main/resources/templates/public/education.html`](#portfolio-app-src-main-resources-templates-public-educationhtml)
- [`portfolio-app/src/main/resources/templates/public/experience.html`](#portfolio-app-src-main-resources-templates-public-experiencehtml)
- [`portfolio-app/src/main/resources/templates/public/explore.html`](#portfolio-app-src-main-resources-templates-public-explorehtml)
- [`portfolio-app/src/main/resources/templates/public/index.html`](#portfolio-app-src-main-resources-templates-public-indexhtml)
- [`portfolio-app/src/main/resources/templates/public/project-details.html`](#portfolio-app-src-main-resources-templates-public-project-detailshtml)
- [`portfolio-app/src/main/resources/templates/public/projects.html`](#portfolio-app-src-main-resources-templates-public-projectshtml)
- [`portfolio-app/src/main/resources/templates/public/services.html`](#portfolio-app-src-main-resources-templates-public-serviceshtml)
- [`portfolio-app/src/main/resources/templates/public/skills.html`](#portfolio-app-src-main-resources-templates-public-skillshtml)

### 13. Admin Panel Templates
- [`portfolio-app/src/main/resources/templates/admin/achievement-form.html`](#portfolio-app-src-main-resources-templates-admin-achievement-formhtml)
- [`portfolio-app/src/main/resources/templates/admin/achievement-list.html`](#portfolio-app-src-main-resources-templates-admin-achievement-listhtml)
- [`portfolio-app/src/main/resources/templates/admin/certification-form.html`](#portfolio-app-src-main-resources-templates-admin-certification-formhtml)
- [`portfolio-app/src/main/resources/templates/admin/certification-list.html`](#portfolio-app-src-main-resources-templates-admin-certification-listhtml)
- [`portfolio-app/src/main/resources/templates/admin/dashboard.html`](#portfolio-app-src-main-resources-templates-admin-dashboardhtml)
- [`portfolio-app/src/main/resources/templates/admin/education-form.html`](#portfolio-app-src-main-resources-templates-admin-education-formhtml)
- [`portfolio-app/src/main/resources/templates/admin/education-list.html`](#portfolio-app-src-main-resources-templates-admin-education-listhtml)
- [`portfolio-app/src/main/resources/templates/admin/experience-form.html`](#portfolio-app-src-main-resources-templates-admin-experience-formhtml)
- [`portfolio-app/src/main/resources/templates/admin/experience-list.html`](#portfolio-app-src-main-resources-templates-admin-experience-listhtml)
- [`portfolio-app/src/main/resources/templates/admin/login.html`](#portfolio-app-src-main-resources-templates-admin-loginhtml)
- [`portfolio-app/src/main/resources/templates/admin/message-list.html`](#portfolio-app-src-main-resources-templates-admin-message-listhtml)
- [`portfolio-app/src/main/resources/templates/admin/message-view.html`](#portfolio-app-src-main-resources-templates-admin-message-viewhtml)
- [`portfolio-app/src/main/resources/templates/admin/project-form.html`](#portfolio-app-src-main-resources-templates-admin-project-formhtml)
- [`portfolio-app/src/main/resources/templates/admin/project-list.html`](#portfolio-app-src-main-resources-templates-admin-project-listhtml)
- [`portfolio-app/src/main/resources/templates/admin/settings.html`](#portfolio-app-src-main-resources-templates-admin-settingshtml)
- [`portfolio-app/src/main/resources/templates/admin/skill-form.html`](#portfolio-app-src-main-resources-templates-admin-skill-formhtml)
- [`portfolio-app/src/main/resources/templates/admin/skill-list.html`](#portfolio-app-src-main-resources-templates-admin-skill-listhtml)

### 14. Error Page Templates
- [`portfolio-app/src/main/resources/templates/error/404.html`](#portfolio-app-src-main-resources-templates-error-404html)
- [`portfolio-app/src/main/resources/templates/error/500.html`](#portfolio-app-src-main-resources-templates-error-500html)
- [`portfolio-app/src/main/resources/templates/error/access-denied.html`](#portfolio-app-src-main-resources-templates-error-access-deniedhtml)
- [`portfolio-app/src/main/resources/templates/error/error.html`](#portfolio-app-src-main-resources-templates-error-errorhtml)

### 15. Styles & Scripts
- [`portfolio-app/src/main/resources/static/css/style.css`](#portfolio-app-src-main-resources-static-css-stylecss)
- [`portfolio-app/src/main/resources/static/css/admin.css`](#portfolio-app-src-main-resources-static-css-admincss)
- [`portfolio-app/src/main/resources/static/js/app.js`](#portfolio-app-src-main-resources-static-js-appjs)

---

# 1. Build & Database Configuration

## `portfolio-app/pom.xml`
<a id="portfolio-app-pomxml"></a>

```xml
<?xml version="1.0" encoding="UTF-8"?>
<project xmlns="http://maven.apache.org/POM/4.0.0"
         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
         xsi:schemaLocation="http://maven.apache.org/POM/4.0.0 https://maven.apache.org/xsd/maven-4.0.0.xsd">
    <modelVersion>4.0.0</modelVersion>

    <!-- ===================================================================
         PERSONAL PORTFOLIO WEB APPLICATION
         ===============================================================
         Parent POM : Spring Boot 3.5.x (brings in dependency management)
         Java       : 21
         Packaging  : jar (runnable with `mvn spring-boot:run`)
         =================================================================== -->
    <parent>
        <groupId>org.springframework.boot</groupId>
        <artifactId>spring-boot-starter-parent</artifactId>
        <version>3.5.16</version>
        <relativePath/> <!-- lookup parent from repository, not from disk -->
    </parent>

    <groupId>com.portfolio</groupId>
    <artifactId>portfolio</artifactId>
    <version>1.0.0</version>
    <name>Personal Portfolio</name>
    <description>Personal Portfolio Web Application built with Spring Boot, Thymeleaf and MySQL</description>

    <properties>
        <java.version>17</java.version>
        <project.build.sourceEncoding>UTF-8</project.build.sourceEncoding>
    </properties>

    <dependencies>

        <!-- ============ WEB (Spring MVC + embedded Tomcat) ============ -->
        <dependency>
            <groupId>org.springframework.boot</groupId>
            <artifactId>spring-boot-starter-web</artifactId>
        </dependency>

        <!-- ============ THYMELEAF (server side templates) ============ -->
        <dependency>
            <groupId>org.springframework.boot</groupId>
            <artifactId>spring-boot-starter-thymeleaf</artifactId>
        </dependency>

        <!-- ============ Spring Security Thymeleaf dialect ============ -->
        <!-- allows sec:authorize / sec:authentication inside templates -->
        <dependency>
            <groupId>org.thymeleaf.extras</groupId>
            <artifactId>thymeleaf-extras-springsecurity6</artifactId>
        </dependency>

        <!-- ============ JPA + HIBERNATE (ORM layer) ============ -->
        <dependency>
            <groupId>org.springframework.boot</groupId>
            <artifactId>spring-boot-starter-data-jpa</artifactId>
        </dependency>

        <!-- ============ SPRING SECURITY (authentication/authorization) == -->
        <dependency>
            <groupId>org.springframework.boot</groupId>
            <artifactId>spring-boot-starter-security</artifactId>
        </dependency>

        <!-- ============ BEAN VALIDATION (jakarta validation) ============ -->
        <dependency>
            <groupId>org.springframework.boot</groupId>
            <artifactId>spring-boot-starter-validation</artifactId>
        </dependency>

        <!-- ============ MYSQL DRIVER ============ -->
        <dependency>
            <groupId>com.mysql</groupId>
            <artifactId>mysql-connector-j</artifactId>
            <scope>runtime</scope>
        </dependency>

        <!-- ============ H2 (in-memory) : ONLY for the demo profile =======
             Lets you demo the app without installing MySQL.
             The default profile is MySQL.                                       -->
        <dependency>
            <groupId>com.h2database</groupId>
            <artifactId>h2</artifactId>
            <scope>runtime</scope>
        </dependency>

        <!-- ============ TESTING ============ -->
        <dependency>
            <groupId>org.springframework.boot</groupId>
            <artifactId>spring-boot-starter-test</artifactId>
            <scope>test</scope>
        </dependency>
        <dependency>
            <groupId>org.springframework.security</groupId>
            <artifactId>spring-security-test</artifactId>
            <scope>test</scope>
        </dependency>

    </dependencies>

    <build>
        <finalName>portfolio</finalName>
        <plugins>
            <plugin>
                <groupId>org.springframework.boot</groupId>
                <artifactId>spring-boot-maven-plugin</artifactId>
            </plugin>
        </plugins>
    </build>
</project>

```

---

## `portfolio-app/database-setup.sql`
<a id="portfolio-app-database-setupsql"></a>

```sql
-- ============================================================================
--  PERSONAL PORTFOLIO - MySQL SETUP SCRIPT
-- ============================================================================
--  Run this ONCE before starting the application:
--
--      mysql -u root -p < database-setup.sql
--
--  It creates the empty database and a dedicated user for the application.
--  The TABLES are created automatically by Hibernate on the first start
--  (spring.jpa.hibernate.ddl-auto=update), so you do not need to create them
--  by hand.
--
--  If you change the user name or password here, remember to change them in
--  src/main/resources/application.properties too (or set the DB_USERNAME and
--  DB_PASSWORD environment variables).
-- ============================================================================

-- 1. THE DATABASE
--    utf8mb4 gives full Unicode support, including emoji in project titles.
CREATE DATABASE IF NOT EXISTS portfolio_db
    CHARACTER SET utf8mb4
    COLLATE utf8mb4_unicode_ci;

-- 2. THE APPLICATION USER
CREATE USER IF NOT EXISTS 'portfolio'@'localhost' IDENTIFIED BY 'portfolio123';
CREATE USER IF NOT EXISTS 'portfolio'@'%'         IDENTIFIED BY 'portfolio123';

-- 3. PERMISSIONS
--    Only this database is granted - never GRANT ALL ON *.* in a real system.
GRANT ALL PRIVILEGES ON portfolio_db.* TO 'portfolio'@'localhost';
GRANT ALL PRIVILEGES ON portfolio_db.* TO 'portfolio'@'%';

FLUSH PRIVILEGES;

-- ============================================================================
--  VERIFY
-- ============================================================================
--  SHOW DATABASES LIKE 'portfolio_db';
--  SELECT user, host FROM mysql.user WHERE user = 'portfolio';
--
--  AFTER the application has started once, the nine tables will exist:
--
--  USE portfolio_db;
--  SHOW TABLES;
--
--      admin_users        certifications     contact_messages
--      educations         experiences        projects
--      site_settings      skills             achievements
--
--  USEFUL QUERIES
--
--  -- How many rows in each table?
--  SELECT 'projects'         AS t, COUNT(*) AS n FROM projects
--  UNION ALL SELECT 'skills',           COUNT(*) FROM skills
--  UNION ALL SELECT 'educations',       COUNT(*) FROM educations
--  UNION ALL SELECT 'experiences',      COUNT(*) FROM experiences
--  UNION ALL SELECT 'certifications',   COUNT(*) FROM certifications
--  UNION ALL SELECT 'achievements',     COUNT(*) FROM achievements
--  UNION ALL SELECT 'contact_messages', COUNT(*) FROM contact_messages
--  UNION ALL SELECT 'site_settings',    COUNT(*) FROM site_settings
--  UNION ALL SELECT 'admin_users',      COUNT(*) FROM admin_users;
--
--  -- Who is logged into the admin panel?
--  SELECT id, username, role, enabled, created_at FROM admin_users;
--
--  -- Newest contact messages
--  SELECT id, name, email, subject, created_at, read_status
--  FROM contact_messages ORDER BY created_at DESC LIMIT 10;
--
--  -- Reset everything and start again with fresh sample data
--  -- (the seeder re-inserts on the next start because the tables are empty)
--  -- DROP DATABASE portfolio_db;   then re-run this script.
-- ============================================================================

```

---

## `portfolio-app/src/main/resources/application.properties`
<a id="portfolio-app-src-main-resources-applicationproperties"></a>

```properties
# ============================================================================
#  PERSONAL PORTFOLIO - MAIN CONFIGURATION  (default profile = MySQL)
# ============================================================================
#  Every value written as  ${ENV_NAME:default}  means:
#     "use the environment variable ENV_NAME if it is set, otherwise use
#      the default after the colon".
#  That is how you keep secrets (database password, admin password) out of
#  the source code while the project still runs out of the box.
# ============================================================================

spring.application.name=portfolio
server.port=${SERVER_PORT:8081}

# ----------------------------------------------------------------------------
#  1. DATABASE  (MySQL)
# ----------------------------------------------------------------------------
#  >>> CHANGE THESE THREE LINES TO MATCH YOUR OWN MYSQL INSTALLATION <<<
#
#  You can also override them without editing this file, for example:
#     Windows :  set DB_URL=jdbc:mysql://localhost:3306/portfolio_db
#     Linux/Mac:  DB_URL=jdbc:mysql://localhost:3306/portfolio_db mvn spring-boot:run
#     IntelliJ :  Run Configuration -> Environment variables

spring.datasource.url=${DB_URL:jdbc:mysql://localhost:3306/portfolio_db?useSSL=false&allowPublicKeyRetrieval=true&serverTimezone=Asia/Kolkata&createDatabaseIfNotExist=true}
spring.datasource.username=${DB_USERNAME:portfolio}
spring.datasource.password=${DB_PASSWORD:portfolio123}
spring.datasource.driver-class-name=com.mysql.cj.jdbc.Driver

# Connection pool (HikariCP - the Spring Boot default)
spring.datasource.hikari.maximum-pool-size=10
spring.datasource.hikari.minimum-idle=2
spring.datasource.hikari.connection-timeout=30000

# ----------------------------------------------------------------------------
#  2. JPA / HIBERNATE
# ----------------------------------------------------------------------------
#  ddl-auto=update  -> Hibernate creates the tables from the @Entity classes
#                      and adds missing columns on later runs. It never drops
#                      a column, so your data survives a restart.
#                      Use "validate" or "none" in a real production system.
#
#  show-sql=true    -> prints every SQL statement to the console. Very useful
#                      while learning; set it to false for better performance.

spring.jpa.hibernate.ddl-auto=update
spring.jpa.show-sql=${SHOW_SQL:true}
spring.jpa.properties.hibernate.format_sql=true

# Naming the dialect explicitly is good practice: Hibernate then does not have
# to open a connection at start-up just to ask the database which flavour it
# is. It also avoids a warning on MariaDB, whose metadata tables differ
# slightly from MySQL's.
#   MySQL 8 / 9   -> org.hibernate.dialect.MySQLDialect      (recommended)
#   MySQL 5.7     -> org.hibernate.dialect.MySQLDialect
#   MariaDB       -> org.hibernate.dialect.MariaDBDialect
spring.jpa.database-platform=${DB_DIALECT:org.hibernate.dialect.MySQLDialect}
spring.jpa.open-in-view=false
spring.jpa.properties.hibernate.jdbc.time_zone=Asia/Kolkata

# ----------------------------------------------------------------------------
#  3. THYMELEAF
# ----------------------------------------------------------------------------
#  cache=false -> templates are re-read on every request, so you can edit an
#                 HTML file and just refresh the browser (no restart needed).
#                 Set it to true when you deploy.

spring.thymeleaf.cache=false
spring.thymeleaf.encoding=UTF-8
spring.thymeleaf.mode=HTML

# ----------------------------------------------------------------------------
#  4. FILE UPLOADS  (project images, certificates, profile photo)
# ----------------------------------------------------------------------------
#  app.upload.dir is read by FileStorageService and mapped to /uploads/**
#  by WebConfig. Keep it OUTSIDE src/main/resources: everything inside
#  target/classes is deleted on every rebuild.

app.upload.dir=${UPLOAD_DIR:./uploads}
spring.servlet.multipart.max-file-size=5MB
spring.servlet.multipart.max-request-size=25MB
spring.servlet.multipart.enabled=true

# ----------------------------------------------------------------------------
#  5. RESUME
# ----------------------------------------------------------------------------
#  Classpath location of the resume served by the "Download Resume" button.
#  Put your own PDF at  src/main/resources/static/files/portfolio-resume.pdf
#  or point this property at a different file name.

app.resume.file=${RESUME_FILE:static/files/portfolio-resume.pdf}

# ----------------------------------------------------------------------------
#  6. SECURITY  -  the admin account created on the first start
# ----------------------------------------------------------------------------
#  >>> NOTHING IS HARD-CODED IN JAVA <<<
#  DataSeeder reads these two properties and stores a BCrypt hash of the
#  password in the admin_users table. Override them with environment
#  variables so your real password never lands in a Git repository:
#
#     Windows :  set ADMIN_PASSWORD=MySecret123
#     Linux/Mac:  ADMIN_PASSWORD=MySecret123 mvn spring-boot:run
#     IntelliJ :  Run Configuration -> Environment variables -> ADMIN_PASSWORD
#
#  With the defaults below the first login is:  admin / ChangeMe@123
#  Change it immediately at  Admin -> Settings -> Change Password.

app.security.default-admin-username=${ADMIN_USERNAME:vaishnavi}
app.security.default-admin-password=${ADMIN_PASSWORD:ChangeMe@123}

# ----------------------------------------------------------------------------
#  7. SAMPLE DATA
# ----------------------------------------------------------------------------
#  true  -> sample projects / skills / education / ... are inserted when the
#           tables are empty (great for a demonstration).
#  false -> start with an empty portfolio.
#  Existing rows are NEVER overwritten, whatever this is set to.

app.seed.enabled=${SEED_DATA:true}

# ----------------------------------------------------------------------------
#  8. SESSION
# ----------------------------------------------------------------------------
server.servlet.session.timeout=30m
server.servlet.session.cookie.http-only=true
server.error.whitelabel.enabled=false

# ----------------------------------------------------------------------------
#  9. LOGGING
# ----------------------------------------------------------------------------
logging.level.root=INFO
logging.level.com.portfolio=INFO
# SQL logging level. Use DEBUG to print every statement, INFO/OFF to quieten it.
# NOTE: this must be a LEVEL (DEBUG/INFO/WARN/ERROR/OFF), not true/false.
logging.level.org.hibernate.SQL=${SQL_LOG_LEVEL:INFO}
logging.level.org.hibernate.orm.jdbc.bind=${SQL_LOG_LEVEL:INFO}

# ----------------------------------------------------------------------------
#  HOW TO RUN WITHOUT MYSQL (demo profile, in-memory H2 database)
# ----------------------------------------------------------------------------
#     mvn spring-boot:run "-Dspring-boot.run.profiles=demo"
#  That switches to src/main/resources/application-demo.properties.

```

---

## `portfolio-app/src/main/resources/application-demo.properties`
<a id="portfolio-app-src-main-resources-application-demoproperties"></a>

```properties
# ============================================================================
#  DEMO PROFILE  -  in-memory H2 database (no MySQL installation required)
# ============================================================================
#  Activate it with:
#     mvn spring-boot:run "-Dspring-boot.run.profiles=demo"
#  or in IntelliJ: Run Configuration -> Active profiles -> demo
#
#  The data lives in memory only, so it disappears when you stop the app and
#  is re-seeded on the next start. Useful for a quick demonstration or for
#  marking the project on a machine without MySQL.
#
#  THE DEFAULT PROFILE IS MYSQL - see application.properties.
# ============================================================================

spring.datasource.url=jdbc:h2:mem:portfolio;DB_CLOSE_DELAY=-1;DB_CLOSE_ON_EXIT=FALSE
spring.datasource.username=sa
spring.datasource.password=
spring.datasource.driver-class-name=org.h2.Driver

spring.jpa.database-platform=org.hibernate.dialect.H2Dialect
spring.jpa.hibernate.ddl-auto=create-drop
spring.jpa.show-sql=false

# H2 web console: http://localhost:8080/h2-console
spring.h2.console.enabled=true
spring.h2.console.path=/h2-console

app.seed.enabled=true

```

---

## `start-portfolio.bat`
<a id="start-portfoliobat"></a>

```cmd
@echo off
title Vaishnavi Mali - Personal Portfolio
echo ====================================================
echo Starting Vaishnavi Mali's Portfolio Web Application
echo ====================================================
echo Web URL:    http://localhost:8081
echo Admin URL:  http://localhost:8081/admin/login
echo Username:   vaishnavi
echo Password:   ChangeMe@123
echo ====================================================

"C:\Users\Vaishnavi\AppData\Local\Programs\DataGrip 2026.2.2\jbr\bin\java.exe" -jar "%~dp0portfolio-app\target\portfolio.jar"
pause

```

---

## `stop-portfolio.bat`
<a id="stop-portfoliobat"></a>

```cmd
@echo off
title Stop Personal Portfolio
echo Stopping Personal Portfolio Application running on port 8081...
for /f "tokens=5" %%a in ('netstat -aon ^| findstr ":8081" ^| findstr "LISTENING"') do (
    echo Terminating PID: %%a
    taskkill /F /PID %%a
)
echo Portfolio application stopped.
pause

```

---

# 2. Main Application & Framework Config

## `portfolio-app/src/main/java/com/portfolio/PortfolioApplication.java`
<a id="portfolio-app-src-main-java-com-portfolio-portfolioapplicationjava"></a>

```java
package com.portfolio;

import org.springframework.boot.SpringApplication;
import org.springframework.boot.autoconfigure.SpringBootApplication;

/**
 * ============================================================================
 * PERSONAL PORTFOLIO WEB APPLICATION - Main Entry Point
 * ============================================================================
 *
 * The {@code @SpringBootApplication} annotation is a shortcut for three things:
 *
 *   1. {@code @SpringBootConfiguration} -> this class holds configuration
 *   2. {@code @EnableAutoConfiguration} -> Spring Boot configures itself
 *   3. {@code @ComponentScan}           -> scans the "com.portfolio" package
 *
 * Because this class lives in the package {@code com.portfolio}, every
 * sub-package (controller, service, repository, entity, config, security ...)
 * is scanned automatically.
 *
 * HOW TO RUN
 *   mvn spring-boot:run          (default profile = MySQL)
 *   mvn spring-boot:run -Dspring-boot.run.profiles=demo   (H2 in-memory DB)
 *
 * Then open http://localhost:8080 in Chrome / Edge / Firefox.
 * ============================================================================
 */
@SpringBootApplication
public class PortfolioApplication {

    public static void main(String[] args) {
        SpringApplication.run(PortfolioApplication.class, args);
    }
}

```

---

## `portfolio-app/src/main/java/com/portfolio/config/SecurityConfig.java`
<a id="portfolio-app-src-main-java-com-portfolio-config-securityconfigjava"></a>

```java
package com.portfolio.config;

import org.springframework.context.annotation.Bean;
import org.springframework.context.annotation.Configuration;
import org.springframework.security.config.annotation.web.builders.HttpSecurity;
import org.springframework.security.config.annotation.web.configuration.EnableWebSecurity;
import org.springframework.security.crypto.bcrypt.BCryptPasswordEncoder;
import org.springframework.security.crypto.password.PasswordEncoder;
import org.springframework.security.web.SecurityFilterChain;

/**
 * ============================================================================
 * SECURITY CONFIGURATION
 * ============================================================================
 * This single class replaces the old (Spring Boot 2) way of extending
 * WebSecurityConfigurerAdapter, which was removed in Spring Security 6.
 *
 * WHAT IT DOES
 *   1. passwordEncoder()  -> BCrypt, the industry standard one-way hash
 *   2. securityFilterChain() -> which URLs are public, which need ROLE_ADMIN,
 *      where the login page is, where logout sends you, and how access
 *      denied / login failures are handled.
 *
 * URL RULES (order matters - first match wins)
 *   / , /css/** , /js/** , /img/** , /uploads/** , /api/**  -> public
 *   /admin/login , /admin/logout                           -> public
 *   /admin/**                                              -> ROLE_ADMIN only
 *   anything else                                          -> authenticated
 * ============================================================================
 */
@Configuration
@EnableWebSecurity
public class SecurityConfig {

    /**
     * PASSWORD ENCODER
     * BCrypt hashes the password with a random salt every time, so the same
     * password produces a different hash each run. The database therefore
     * never contains a readable password, and nothing in the Java source
     * contains one either.
     */
    @Bean
    public PasswordEncoder passwordEncoder() {
        return new BCryptPasswordEncoder();
    }

    @Bean
    public SecurityFilterChain securityFilterChain(HttpSecurity http) throws Exception {
        http
                // ---------------------------------------------------------
                // AUTHORIZATION : who may open which URL
                // ---------------------------------------------------------
                .authorizeHttpRequests(auth -> auth
                        // Static resources and public routes
                        .requestMatchers(
                                "/", "/home", "/about", "/skills", "/projects", "/projects/**",
                                "/education", "/experience", "/certifications", "/achievements",
                                "/services", "/contact", "/contact/submit", "/resume",
                                "/explore", "/u/**", "/login", "/register", "/register/submit",
                                "/css/**", "/js/**", "/img/**", "/uploads/**", "/webjars/**",
                                "/favicon.ico", "/error", "/api/**", "/h2-console/**"
                        ).permitAll()

                        // Legacy / admin login URLs
                        .requestMatchers("/admin/login", "/admin/logout").permitAll()

                        // Dashboard and admin panels require authentication
                        .requestMatchers("/admin/**").authenticated()

                        .anyRequest().permitAll()
                )

                // ---------------------------------------------------------
                // FORM LOGIN : email or username login
                // ---------------------------------------------------------
                .formLogin(form -> form
                        .loginPage("/login")
                        .loginProcessingUrl("/login")
                        .usernameParameter("emailOrUsername")
                        .passwordParameter("password")
                        .defaultSuccessUrl("/admin/dashboard", true)
                        .failureUrl("/login?error=true")
                        .permitAll()
                )

                // ---------------------------------------------------------
                // LOGOUT
                // ---------------------------------------------------------
                .logout(logout -> logout
                        .logoutRequestMatcher(
                                new org.springframework.security.web.util.matcher.OrRequestMatcher(
                                        new org.springframework.security.web.util.matcher.AntPathRequestMatcher("/logout"),
                                        new org.springframework.security.web.util.matcher.AntPathRequestMatcher("/admin/logout")
                                ))
                        .invalidateHttpSession(true)
                        .deleteCookies("JSESSIONID")
                        .logoutSuccessUrl("/login?logout=true")
                        .permitAll()
                )

                // ---------------------------------------------------------
                // ACCESS DENIED / SESSION
                // ---------------------------------------------------------
                .exceptionHandling(ex -> ex
                        // A logged-in user who opens a forbidden URL.
                        .accessDeniedPage("/error/access-denied")
                )
                // ---------------------------------------------------------
                // CSRF & HEADERS (Enable H2 Console for Demo Profile)
                // ---------------------------------------------------------
                .csrf(csrf -> csrf
                        .ignoringRequestMatchers("/h2-console/**")
                )
                .headers(headers -> headers
                        .frameOptions(frame -> frame.sameOrigin())
                )
                .sessionManagement(session -> session
                        // One admin session at a time keeps the demo tidy.
                        .maximumSessions(1)
                        .maxSessionsPreventsLogin(false)
                );

        return http.build();
    }
}

```

---

## `portfolio-app/src/main/java/com/portfolio/config/WebConfig.java`
<a id="portfolio-app-src-main-java-com-portfolio-config-webconfigjava"></a>

```java
package com.portfolio.config;

import org.springframework.beans.factory.annotation.Value;
import org.springframework.context.annotation.Configuration;
import org.springframework.web.servlet.config.annotation.ResourceHandlerRegistry;
import org.springframework.web.servlet.config.annotation.WebMvcConfigurer;

import java.nio.file.Paths;

/**
 * ============================================================================
 * WEB CONFIGURATION
 * ============================================================================
 * Implements {@code WebMvcConfigurer} to customise Spring MVC without
 * replacing its defaults.
 *
 * THE ONE THING IT ADDS
 *   Uploaded images live in a folder OUTSIDE the jar (see app.upload.dir).
 *   Spring Boot only serves files from the classpath by default, so we map
 *   the URL prefix /uploads/** to that folder on disk.
 *
 *   Result: a file saved at ./uploads/abc.png is reachable at
 *           http://localhost:8080/uploads/abc.png
 * ============================================================================
 */
@Configuration
public class WebConfig implements WebMvcConfigurer {

    @Value("${app.upload.dir:./uploads}")
    private String uploadDir;

    @Override
    public void addResourceHandlers(ResourceHandlerRegistry registry) {
        String location = Paths.get(uploadDir).toAbsolutePath().normalize().toUri().toString();
        if (!location.endsWith("/")) {
            location += "/";
        }
        registry.addResourceHandler("/uploads/**")
                .addResourceLocations(location)
                // Browsers may cache uploaded images for one day.
                .setCachePeriod(86400);
    }
}

```

---

## `portfolio-app/src/main/java/com/portfolio/config/GlobalModelAttributes.java`
<a id="portfolio-app-src-main-java-com-portfolio-config-globalmodelattributesjava"></a>

```java
package com.portfolio.config;

import com.portfolio.service.DashboardService;
import com.portfolio.service.SiteSettingService;
import org.springframework.web.bind.annotation.ControllerAdvice;
import org.springframework.web.bind.annotation.ModelAttribute;

import java.util.Map;

/**
 * ============================================================================
 * GLOBAL MODEL ATTRIBUTES
 * ============================================================================
 * A second use of {@code @ControllerAdvice}: the methods marked with
 * {@code @ModelAttribute} run BEFORE every controller method, so their values
 * are available in every Thymeleaf template without each controller having to
 * add them.
 *
 * This is what lets the navbar and footer use {@code ${settings['hero.name']}}
 * and the admin sidebar use {@code ${unreadMessages}} without any extra code
 * in the controllers.
 * ============================================================================
 */
@ControllerAdvice
public class GlobalModelAttributes {

    private final SiteSettingService siteSettingService;
    private final DashboardService dashboardService;
    private final com.portfolio.security.AuthHelper authHelper;

    public GlobalModelAttributes(SiteSettingService siteSettingService,
                                 DashboardService dashboardService,
                                 com.portfolio.security.AuthHelper authHelper) {
        this.siteSettingService = siteSettingService;
        this.dashboardService = dashboardService;
        this.authHelper = authHelper;
    }

    /** Expose currently authenticated user to all Thymeleaf templates. */
    @ModelAttribute("currentUser")
    public com.portfolio.entity.AdminUser currentUser() {
        return authHelper.getCurrentUserOptional().orElse(null);
    }

    /** Every profile setting as a Map -> ${settings['hero.name']} etc. */
    @ModelAttribute("settings")
    public Map<String, String> settings() {
        return authHelper.getCurrentUserOptional()
                .map(siteSettingService::getSettingsMap)
                .orElseGet(siteSettingService::getSettingsMap);
    }

    /** The "What I Do" cards - used by the home page and the services page. */
    @ModelAttribute("services")
    public Object services() {
        return authHelper.getCurrentUserOptional()
                .map(siteSettingService::getServices)
                .orElseGet(siteSettingService::getServices);
    }

    /** Unread message counter -> the red badge in the admin sidebar. */
    @ModelAttribute("unreadMessages")
    public long unreadMessages() {
        return authHelper.getCurrentUserOptional()
                .map(dashboardService::getUnreadMessageCount)
                .orElseGet(dashboardService::getUnreadMessageCount);
    }

    /** Current year, so the footer copyright never goes stale. */
    @ModelAttribute("currentYear")
    public int currentYear() {
        return java.time.Year.now().getValue();
    }
}

```

---

## `portfolio-app/src/main/java/com/portfolio/config/PortfolioProfileData.java`
<a id="portfolio-app-src-main-java-com-portfolio-config-portfolioprofiledatajava"></a>

```java
package com.portfolio.config;

import com.portfolio.entity.Project;
import com.portfolio.entity.ProjectCategory;
import com.portfolio.entity.Skill;

import java.util.List;

/**
 * ============================================================================
 * CENTRALIZED PORTFOLIO PROFILE DATA
 * ============================================================================
 * ONE central place defining the owner profile details, defaults, and seed
 * data for the portfolio application.
 *
 * If you ever need to update your name, email, location, branch, bio, or
 * initial project/skill details, you can edit them right here in this file!
 * ============================================================================
 */
public final class PortfolioProfileData {

    private PortfolioProfileData() {
        // Prevent instantiation
    }

    // =========================================================================
    //  1. CORE OWNER INFORMATION
    // =========================================================================
    public static final String FULL_NAME = "Vaishnavi Sunil Mali";
    public static final String FIRST_NAME = "Vaishnavi";
    public static final String DEFAULT_USERNAME = "vaishnavi";
    public static final String EMAIL = "vaishnavim25extc@student.mes.ac.in";
    public static final String LOCATION = "Kharghar, Mumbai, Maharashtra, India";
    public static final String BRANCH = "Electronics and Telecommunication Engineering (EXTC)";
    public static final String HEADLINE = "EXTC Engineering Student & Developer";
    public static final String PHONE = ""; // Editable from admin panel

    public static final String SHORT_INTRO =
            "Electronics and Telecommunication Engineering student interested in technology, software development and building practical projects.";

    public static final String TYPING_WORDS =
            "EXTC Engineering Student,Java Developer,IoT & Embedded Systems Enthusiast,Problem Solver";

    public static final String ABOUT_INTRO =
            "Hello! I am Vaishnavi Sunil Mali, an Electronics and Telecommunication Engineering (EXTC) student based in Kharghar, Mumbai. "
                    + "I am passionate about technology, software development, and bridging hardware-software systems through practical, impactful projects.";

    public static final String CAREER_OBJECTIVE =
            "Aspiring software and technology engineer seeking opportunities to apply my analytical abilities, programming fundamentals, "
                    + "and engineering principles to develop reliable, high-performance applications and practical hardware-software solutions.";

    public static final String TECHNICAL_INTERESTS =
            "Core Java, Python, Web Development, Internet of Things (IoT), Digital Communication Systems, Microprocessors, MySQL Database Management";

    public static final String LANGUAGES = "English, Hindi, Marathi";

    // Social URLs - left empty by default to prevent fake/broken links.
    // Can be configured from Admin -> Settings at any time.
    public static final String GITHUB_URL = "";
    public static final String LINKEDIN_URL = "";
    public static final String TWITTER_URL = "";
    public static final String INSTAGRAM_URL = "";
    public static final String RESUME_URL = "/resume";
    public static final String PROFILE_IMAGE_URL = "/img/profile-placeholder.svg";

    // Services - one per line: icon|title|description
    public static final String SERVICES =
            "cpu|IoT & Embedded Systems|Building smart sensor monitoring setups with microcontrollers, sensor integration, and real-time alerts.\n"
                    + "code|Java Development|Developing robust Java applications, modular backend systems, and database-driven solutions.\n"
                    + "globe|Web Development|Designing responsive, clean web interfaces with HTML, CSS, JavaScript, and Spring Boot Thymeleaf.\n"
                    + "database|Database Management|Structuring relational MySQL databases, writing SQL queries, and integrating persistence layers.";

    // =========================================================================
    //  2. EDUCATION DETAILS
    // =========================================================================
    public static final String EDU_DEGREE = "B.E. in Electronics and Telecommunication Engineering (EXTC)";
    public static final String EDU_INSTITUTION = "Pillai College of Engineering, New Panvel (Mumbai University)";
    public static final int EDU_START_YEAR = 2022;
    public static final int EDU_END_YEAR = 2026;
    public static final String EDU_YEAR_RANGE = "2022 - 2026";
    public static final String EDU_CGPA = "8.5 CGPA";
    public static final String EDU_DESCRIPTION =
            "Coursework covering digital electronics, microprocessors, communication systems, programming, and data networks.";

    // =========================================================================
    //  3. REAL SAMPLE PROJECTS
    // =========================================================================
    public static List<Project> createDefaultProjects() {
        return List.of(
                new Project(
                        "Smart IoT Monitoring System",
                        "Real-time environmental and sensor monitoring system using IoT microcontroller nodes and web telemetry dashboard.",
                        "Manual tracking of environmental conditions across remote facilities is labor-intensive and error-prone. This automated IoT solution provides continuous remote monitoring with instantaneous threshold violation alerts.",
                        "Sensor data telemetry from microcontroller nodes\n"
                                + "Real-time monitoring and threshold alerts\n"
                                + "Web dashboard for live metrics visualization\n"
                                + "Historical sensor data logging and reporting",
                        "IoT, ESP32 / Arduino, Sensors, Java, Spring Boot, MQTT / HTTP, MySQL, Bootstrap",
                        "", "", "/img/project-placeholder.svg",
                        ProjectCategory.IOT, true, 1
                ),
                new Project(
                        "Student Management System",
                        "Full-featured academic records and administrative management application built with Java and relational MySQL database.",
                        "Institutions often rely on disjointed spreadsheets for tracking student records, course registrations, and marks. This centralized system provides secure, role-based CRUD workflows with transactional database integrity.",
                        "Student profile and enrollment management\n"
                                + "Course and semester grade tracking\n"
                                + "Attendance logging with automated summaries\n"
                                + "Role-based access control\n"
                                + "Normalized MySQL database schema with JPA integration",
                        "Java, Spring Boot, MySQL, JDBC / Spring Data JPA, Thymeleaf, Bootstrap",
                        "", "", "/img/project-placeholder.svg",
                        ProjectCategory.JAVA, true, 2
                ),
                new Project(
                        "Personal Portfolio Website",
                        "Dynamic, responsive personal portfolio web application with administrative CMS and multi-user showcase capabilities.",
                        "Static portfolio pages require code updates for every profile change. This application offers a complete web administration portal with secure login, dynamic content management, and responsive presentation.",
                        "Showcase for projects, technical skills, and academic background\n"
                                + "Administrative dashboard for real-time content management\n"
                                + "Responsive layout with dark/light mode toggle\n"
                                + "Interactive contact form with input validation and message tracking\n"
                                + "REST API endpoints for project data",
                        "Java, Spring Boot, Spring Security, Spring Data JPA, Thymeleaf, MySQL, Bootstrap 5",
                        "", "", "/img/project-placeholder.svg",
                        ProjectCategory.WEB, true, 3
                )
        );
    }

    // =========================================================================
    //  4. REAL TECHNICAL SKILLS
    // =========================================================================
    public static List<Skill> createDefaultSkills() {
        return List.of(
                // Programming Languages
                new Skill("Java", "Programming Languages", 90, 1),
                new Skill("Python", "Programming Languages", 80, 2),
                new Skill("C", "Programming Languages", 75, 3),

                // Web Technologies
                new Skill("HTML", "Web Technologies", 90, 1),
                new Skill("CSS", "Web Technologies", 85, 2),
                new Skill("JavaScript", "Web Technologies", 80, 3),

                // Databases
                new Skill("MySQL", "Databases", 85, 1),
                new Skill("SQL", "Databases", 85, 2),

                // Core / EXTC
                new Skill("Digital Electronics", "Core / EXTC", 85, 1),
                new Skill("Communication Systems", "Core / EXTC", 80, 2),
                new Skill("Microprocessors", "Core / EXTC", 80, 3),

                // Tools & Platforms
                new Skill("Git", "Tools & Platforms", 85, 1),
                new Skill("GitHub", "Tools & Platforms", 85, 2),
                new Skill("VS Code", "Tools & Platforms", 90, 3)
        );
    }
}

```

---

# 3. Domain Entities & Enums

## `portfolio-app/src/main/java/com/portfolio/entity/Achievement.java`
<a id="portfolio-app-src-main-java-com-portfolio-entity-achievementjava"></a>

```java
package com.portfolio.entity;

import jakarta.persistence.Column;
import jakarta.persistence.Entity;
import jakarta.persistence.GeneratedValue;
import jakarta.persistence.GenerationType;
import jakarta.persistence.Id;
import jakarta.persistence.Table;
import jakarta.validation.constraints.NotBlank;
import jakarta.validation.constraints.Size;

import java.time.LocalDate;

/**
 * ============================================================================
 * ENTITY : Achievement
 * TABLE  : achievements
 * ============================================================================
 * Hackathons, competitions, awards and academic achievements.
 * The "category" column drives the small coloured pill shown on the card.
 * ============================================================================
 */
@Entity
@Table(name = "achievements")
public class Achievement {

    @Id
    @GeneratedValue(strategy = GenerationType.IDENTITY)
    private Long id;

    @com.fasterxml.jackson.annotation.JsonIgnore
    @jakarta.persistence.ManyToOne(fetch = jakarta.persistence.FetchType.LAZY)
    @jakarta.persistence.JoinColumn(name = "user_id")
    private AdminUser user;

    /** e.g. "1st Place - Smart India Hackathon". */
    @NotBlank(message = "Achievement title is required")
    @Size(max = 160, message = "Title must not exceed 160 characters")
    @Column(nullable = false, length = 160)
    private String title;

    @Size(max = 800, message = "Description must not exceed 800 characters")
    @Column(length = 800)
    private String description;

    @Column(name = "achievement_date")
    private LocalDate achievementDate;

    /** Who gave the award / organised the event. */
    @Size(max = 160, message = "Organization must not exceed 160 characters")
    @Column(length = 160)
    private String organization;

    /** Hackathon / Competition / Award / Academic / Other. */
    @Size(max = 40)
    @Column(length = 40)
    private String category = "Achievement";

    /** Optional link (results page, LinkedIn post, ...). */
    @Size(max = 300)
    @Column(length = 300)
    private String linkUrl;

    /** Lower number = shown first. */
    @Column(nullable = false)
    private int sortOrder = 0;

    // =====================================================================
    //  CONSTRUCTORS
    // =====================================================================

    public Achievement() {
    }

    public Achievement(String title, String description, LocalDate achievementDate,
                       String organization, String category, String linkUrl, int sortOrder) {
        this.title = title;
        this.description = description;
        this.achievementDate = achievementDate;
        this.organization = organization;
        this.category = category;
        this.linkUrl = linkUrl;
        this.sortOrder = sortOrder;
    }

    /** Bootstrap badge colour per category (keeps the view logic-free). */
    public String getBadgeClass() {
        if (category == null) {
            return "text-bg-secondary";
        }
        return switch (category.trim().toLowerCase()) {
            case "hackathon" -> "text-bg-danger";
            case "competition" -> "text-bg-warning";
            case "award" -> "text-bg-success";
            case "academic" -> "text-bg-info";
            default -> "text-bg-secondary";
        };
    }

    // =====================================================================
    //  GETTERS / SETTERS
    // =====================================================================

    public Long getId() {
        return id;
    }

    public void setId(Long id) {
        this.id = id;
    }

    public String getTitle() {
        return title;
    }

    public void setTitle(String title) {
        this.title = title;
    }

    public String getDescription() {
        return description;
    }

    public void setDescription(String description) {
        this.description = description;
    }

    public LocalDate getAchievementDate() {
        return achievementDate;
    }

    public void setAchievementDate(LocalDate achievementDate) {
        this.achievementDate = achievementDate;
    }

    public String getOrganization() {
        return organization;
    }

    public void setOrganization(String organization) {
        this.organization = organization;
    }

    public String getCategory() {
        return category;
    }

    public void setCategory(String category) {
        this.category = category;
    }

    public String getLinkUrl() {
        return linkUrl;
    }

    public void setLinkUrl(String linkUrl) {
        this.linkUrl = linkUrl;
    }

    public int getSortOrder() {
        return sortOrder;
    }

    public void setSortOrder(int sortOrder) {
        this.sortOrder = sortOrder;
    }

    public AdminUser getUser() {
        return user;
    }

    public void setUser(AdminUser user) {
        this.user = user;
    }
}

```

---

## `portfolio-app/src/main/java/com/portfolio/entity/AdminUser.java`
<a id="portfolio-app-src-main-java-com-portfolio-entity-adminuserjava"></a>

```java
package com.portfolio.entity;

import jakarta.persistence.Column;
import jakarta.persistence.Entity;
import jakarta.persistence.GeneratedValue;
import jakarta.persistence.GenerationType;
import jakarta.persistence.Id;
import jakarta.persistence.Table;
import jakarta.validation.constraints.NotBlank;
import jakarta.validation.constraints.Size;

import java.time.LocalDateTime;

/**
 * ============================================================================
 * ENTITY : AdminUser
 * TABLE  : admin_users
 * ============================================================================
 * The login account for the admin panel.
 *
 * ---------------------------------------------------------------------------
 * WHY THE PASSWORD IS NOT HARD-CODED (important - asked for in the project)
 * ---------------------------------------------------------------------------
 * The {@code password} column stores a **BCrypt hash**, never plain text.
 * BCrypt is a one-way hash with a random salt, so even if the database is
 * copied nobody can read the original password.
 *
 * The very first account is created on start-up by
 * {@link com.portfolio.init.DataSeeder} using the value of the property
 * {@code app.security.default-admin-password}, which is read from
 * application.properties (or the ADMIN_PASSWORD environment variable).
 * The admin can change that password at any time from
 * Admin -> Settings -> Change Password, which writes a new BCrypt hash
 * into this table. Nothing in the Java source ever contains a password.
 * ============================================================================
 */
@Entity
@Table(name = "admin_users")
public class AdminUser {

    @Id
    @GeneratedValue(strategy = GenerationType.IDENTITY)
    private Long id;

    @NotBlank(message = "Username is required")
    @Size(min = 3, max = 40, message = "Username must be between 3 and 40 characters")
    @Column(nullable = false, unique = true, length = 40)
    private String username;

    @jakarta.validation.constraints.Email(message = "Please provide a valid email address")
    @NotBlank(message = "Email is required")
    @Column(nullable = false, unique = true, length = 100)
    private String email;

    /** BCrypt hash - 60 characters, e.g. "$2a$10$....". */
    @com.fasterxml.jackson.annotation.JsonIgnore
    @NotBlank
    @Column(nullable = false, length = 100)
    private String password;

    /** Display name shown in the dashboard header. */
    @Size(max = 80)
    @Column(name = "full_name", length = 80)
    private String fullName;

    /** Professional headline or title (e.g., Full Stack Java Developer). */
    @Size(max = 120)
    @Column(length = 120)
    private String headline;

    /** Short bio / about summary. */
    @Column(columnDefinition = "TEXT")
    private String bio;

    @Size(max = 30)
    @Column(length = 30)
    private String phone;

    @Size(max = 100)
    @Column(length = 100)
    private String location;

    @Size(max = 255)
    @Column(name = "avatar_url", length = 255)
    private String avatarUrl;

    @Size(max = 255)
    @Column(name = "github_url", length = 255)
    private String githubUrl;

    @Size(max = 255)
    @Column(name = "linkedin_url", length = 255)
    private String linkedinUrl;

    @Size(max = 255)
    @Column(name = "twitter_url", length = 255)
    private String twitterUrl;

    @Size(max = 255)
    @Column(name = "website_url", length = 255)
    private String websiteUrl;

    /** Spring Security authority, e.g. "ROLE_ADMIN". */
    @NotBlank
    @Column(nullable = false, length = 40)
    private String role = "ROLE_ADMIN";

    /** A disabled account cannot log in (checked by Spring Security). */
    @Column(nullable = false)
    private boolean enabled = true;

    @Column(name = "created_at", nullable = false, updatable = false)
    private LocalDateTime createdAt = LocalDateTime.now();

    // =====================================================================
    //  CONSTRUCTORS
    // =====================================================================

    public AdminUser() {
    }

    public AdminUser(String username, String email, String encodedPassword, String fullName, String role) {
        this.username = username;
        this.email = email;
        this.password = encodedPassword;
        this.fullName = fullName;
        this.role = role;
    }

    public AdminUser(String username, String encodedPassword, String fullName, String role) {
        this.username = username;
        this.email = username + "@portfolio.local";
        this.password = encodedPassword;
        this.fullName = fullName;
        this.role = role;
    }

    // =====================================================================
    //  GETTERS / SETTERS
    // =====================================================================

    public Long getId() {
        return id;
    }

    public void setId(Long id) {
        this.id = id;
    }

    public String getUsername() {
        return username;
    }

    public void setUsername(String username) {
        this.username = username;
    }

    public String getEmail() {
        return email;
    }

    public void setEmail(String email) {
        this.email = email;
    }

    public String getHeadline() {
        return headline;
    }

    public void setHeadline(String headline) {
        this.headline = headline;
    }

    public String getBio() {
        return bio;
    }

    public void setBio(String bio) {
        this.bio = bio;
    }

    public String getPhone() {
        return phone;
    }

    public void setPhone(String phone) {
        this.phone = phone;
    }

    public String getLocation() {
        return location;
    }

    public void setLocation(String location) {
        this.location = location;
    }

    public String getAvatarUrl() {
        return avatarUrl;
    }

    public void setAvatarUrl(String avatarUrl) {
        this.avatarUrl = avatarUrl;
    }

    public String getGithubUrl() {
        return githubUrl;
    }

    public void setGithubUrl(String githubUrl) {
        this.githubUrl = githubUrl;
    }

    public String getLinkedinUrl() {
        return linkedinUrl;
    }

    public void setLinkedinUrl(String linkedinUrl) {
        this.linkedinUrl = linkedinUrl;
    }

    public String getTwitterUrl() {
        return twitterUrl;
    }

    public void setTwitterUrl(String twitterUrl) {
        this.twitterUrl = twitterUrl;
    }

    public String getWebsiteUrl() {
        return websiteUrl;
    }

    public void setWebsiteUrl(String websiteUrl) {
        this.websiteUrl = websiteUrl;
    }

    public String getPassword() {
        return password;
    }

    public void setPassword(String password) {
        this.password = password;
    }

    public String getFullName() {
        return fullName;
    }

    public void setFullName(String fullName) {
        this.fullName = fullName;
    }

    public String getRole() {
        return role;
    }

    public void setRole(String role) {
        this.role = role;
    }

    public boolean isEnabled() {
        return enabled;
    }

    public void setEnabled(boolean enabled) {
        this.enabled = enabled;
    }

    public LocalDateTime getCreatedAt() {
        return createdAt;
    }

    public void setCreatedAt(LocalDateTime createdAt) {
        this.createdAt = createdAt;
    }
}

```

---

## `portfolio-app/src/main/java/com/portfolio/entity/Certification.java`
<a id="portfolio-app-src-main-java-com-portfolio-entity-certificationjava"></a>

```java
package com.portfolio.entity;

import jakarta.persistence.Column;
import jakarta.persistence.Entity;
import jakarta.persistence.GeneratedValue;
import jakarta.persistence.GenerationType;
import jakarta.persistence.Id;
import jakarta.persistence.Table;
import jakarta.validation.constraints.NotBlank;
import jakarta.validation.constraints.Size;

import java.time.LocalDate;

/**
 * ============================================================================
 * ENTITY : Certification
 * TABLE  : certifications
 * ============================================================================
 * One row = one certificate. Both an image and a PDF can be attached:
 *   imageUrl      -> thumbnail shown on the card
 *   certificateUrl-> link opened by the "View Certificate" button
 * ============================================================================
 */
@Entity
@Table(name = "certifications")
public class Certification {

    @Id
    @GeneratedValue(strategy = GenerationType.IDENTITY)
    private Long id;

    @com.fasterxml.jackson.annotation.JsonIgnore
    @jakarta.persistence.ManyToOne(fetch = jakarta.persistence.FetchType.LAZY)
    @jakarta.persistence.JoinColumn(name = "user_id")
    private AdminUser user;

    /** e.g. "Oracle Certified Professional: Java SE 17 Developer". */
    @NotBlank(message = "Certificate title is required")
    @Size(max = 160, message = "Title must not exceed 160 characters")
    @Column(nullable = false, length = 160)
    private String title;

    /** Issuing organization, e.g. "Oracle", "Coursera". */
    @NotBlank(message = "Issuer is required")
    @Size(max = 120, message = "Issuer must not exceed 120 characters")
    @Column(nullable = false, length = 120)
    private String issuer;

    /** Issue date - optional, some certificates have no printed date. */
    @Column(name = "issue_date")
    private LocalDate issueDate;

    /** Link to the certificate PDF or its verification page. */
    @Size(max = 300, message = "Certificate URL must not exceed 300 characters")
    @Column(length = 300)
    private String certificateUrl;

    /** Uploaded certificate image (thumbnail). */
    @Size(max = 300)
    @Column(length = 300)
    private String imageUrl;

    /** Credential ID shown on the card, e.g. "1A2B3C4D". */
    @Size(max = 60)
    @Column(length = 60)
    private String credentialId;

    /** Lower number = shown first. */
    @Column(nullable = false)
    private int sortOrder = 0;

    // =====================================================================
    //  CONSTRUCTORS
    // =====================================================================

    public Certification() {
    }

    public Certification(String title, String issuer, LocalDate issueDate, String certificateUrl,
                         String imageUrl, String credentialId, int sortOrder) {
        this.title = title;
        this.issuer = issuer;
        this.issueDate = issueDate;
        this.certificateUrl = certificateUrl;
        this.imageUrl = imageUrl;
        this.credentialId = credentialId;
        this.sortOrder = sortOrder;
    }

    // =====================================================================
    //  GETTERS / SETTERS
    // =====================================================================

    public Long getId() {
        return id;
    }

    public void setId(Long id) {
        this.id = id;
    }

    public String getTitle() {
        return title;
    }

    public void setTitle(String title) {
        this.title = title;
    }

    public String getIssuer() {
        return issuer;
    }

    public void setIssuer(String issuer) {
        this.issuer = issuer;
    }

    public LocalDate getIssueDate() {
        return issueDate;
    }

    public void setIssueDate(LocalDate issueDate) {
        this.issueDate = issueDate;
    }

    public String getCertificateUrl() {
        return certificateUrl;
    }

    public void setCertificateUrl(String certificateUrl) {
        this.certificateUrl = certificateUrl;
    }

    public String getImageUrl() {
        return imageUrl;
    }

    public void setImageUrl(String imageUrl) {
        this.imageUrl = imageUrl;
    }

    public String getCredentialId() {
        return credentialId;
    }

    public void setCredentialId(String credentialId) {
        this.credentialId = credentialId;
    }

    public int getSortOrder() {
        return sortOrder;
    }

    public void setSortOrder(int sortOrder) {
        this.sortOrder = sortOrder;
    }

    public AdminUser getUser() {
        return user;
    }

    public void setUser(AdminUser user) {
        this.user = user;
    }
}

```

---

## `portfolio-app/src/main/java/com/portfolio/entity/ContactMessage.java`
<a id="portfolio-app-src-main-java-com-portfolio-entity-contactmessagejava"></a>

```java
package com.portfolio.entity;

import jakarta.persistence.Column;
import jakarta.persistence.Entity;
import jakarta.persistence.GeneratedValue;
import jakarta.persistence.GenerationType;
import jakarta.persistence.Id;
import jakarta.persistence.Table;
import jakarta.validation.constraints.Email;
import jakarta.validation.constraints.NotBlank;
import jakarta.validation.constraints.Size;

import java.time.LocalDateTime;

/**
 * ============================================================================
 * ENTITY : ContactMessage
 * TABLE  : contact_messages
 * ============================================================================
 * Every submission of the public contact form becomes one row.
 * The admin can read messages, toggle the read flag and delete them.
 *
 * SECURITY NOTE
 *   The message text is rendered with Thymeleaf's {@code th:text}, which
 *   HTML-escapes its output, so a visitor cannot inject script into the
 *   admin panel through this form (stored XSS).
 * ============================================================================
 */
@Entity
@Table(name = "contact_messages")
public class ContactMessage {

    @Id
    @GeneratedValue(strategy = GenerationType.IDENTITY)
    private Long id;

    @com.fasterxml.jackson.annotation.JsonIgnore
    @jakarta.persistence.ManyToOne(fetch = jakarta.persistence.FetchType.LAZY)
    @jakarta.persistence.JoinColumn(name = "recipient_user_id")
    private AdminUser recipient;

    @NotBlank(message = "Please enter your name")
    @Size(min = 2, max = 80, message = "Name must be between 2 and 80 characters")
    @Column(nullable = false, length = 80)
    private String name;

    @NotBlank(message = "Please enter your email address")
    @Email(message = "Please enter a valid email address")
    @Size(max = 120, message = "Email must not exceed 120 characters")
    @Column(nullable = false, length = 120)
    private String email;

    @NotBlank(message = "Please enter a subject")
    @Size(min = 3, max = 150, message = "Subject must be between 3 and 150 characters")
    @Column(nullable = false, length = 150)
    private String subject;

    @NotBlank(message = "Please write your message")
    @Size(min = 10, max = 2000, message = "Message must be between 10 and 2000 characters")
    @Column(nullable = false, length = 2000)
    private String message;

    @Column(name = "created_at", nullable = false, updatable = false)
    private LocalDateTime createdAt = LocalDateTime.now();

    /** false = new / unread, true = already handled by the admin. */
    @Column(name = "read_status", nullable = false)
    private boolean readStatus = false;

    // =====================================================================
    //  CONSTRUCTORS
    // =====================================================================

    public ContactMessage() {
    }

    public ContactMessage(String name, String email, String subject, String message) {
        this.name = name;
        this.email = email;
        this.subject = subject;
        this.message = message;
    }

    // =====================================================================
    //  GETTERS / SETTERS
    // =====================================================================

    public Long getId() {
        return id;
    }

    public void setId(Long id) {
        this.id = id;
    }

    public String getName() {
        return name;
    }

    public void setName(String name) {
        this.name = name;
    }

    public String getEmail() {
        return email;
    }

    public void setEmail(String email) {
        this.email = email;
    }

    public String getSubject() {
        return subject;
    }

    public void setSubject(String subject) {
        this.subject = subject;
    }

    public String getMessage() {
        return message;
    }

    public void setMessage(String message) {
        this.message = message;
    }

    public LocalDateTime getCreatedAt() {
        return createdAt;
    }

    public void setCreatedAt(LocalDateTime createdAt) {
        this.createdAt = createdAt;
    }

    public boolean isReadStatus() {
        return readStatus;
    }

    public void setReadStatus(boolean readStatus) {
        this.readStatus = readStatus;
    }

    public AdminUser getRecipient() {
        return recipient;
    }

    public void setRecipient(AdminUser recipient) {
        this.recipient = recipient;
    }
}

```

---

## `portfolio-app/src/main/java/com/portfolio/entity/Education.java`
<a id="portfolio-app-src-main-java-com-portfolio-entity-educationjava"></a>

```java
package com.portfolio.entity;

import jakarta.persistence.Column;
import jakarta.persistence.Entity;
import jakarta.persistence.GeneratedValue;
import jakarta.persistence.GenerationType;
import jakarta.persistence.Id;
import jakarta.persistence.Table;
import jakarta.validation.constraints.Max;
import jakarta.validation.constraints.Min;
import jakarta.validation.constraints.NotBlank;
import jakarta.validation.constraints.NotNull;
import jakarta.validation.constraints.Size;

/**
 * ============================================================================
 * ENTITY : Education
 * TABLE  : educations
 * ============================================================================
 * One row = one qualification (Degree / Diploma / School).
 * Rendered as a vertical timeline on the public Education page.
 * ============================================================================
 */
@Entity
@Table(name = "educations")
public class Education {

    @Id
    @GeneratedValue(strategy = GenerationType.IDENTITY)
    private Long id;

    @com.fasterxml.jackson.annotation.JsonIgnore
    @jakarta.persistence.ManyToOne(fetch = jakarta.persistence.FetchType.LAZY)
    @jakarta.persistence.JoinColumn(name = "user_id")
    private AdminUser user;

    /** e.g. "B.E. Computer Engineering". */
    @NotBlank(message = "Degree is required")
    @Size(max = 120, message = "Degree must not exceed 120 characters")
    @Column(nullable = false, length = 120)
    private String degree;

    /** e.g. "XYZ College of Engineering, Pune". */
    @NotBlank(message = "Institution is required")
    @Size(max = 160, message = "Institution must not exceed 160 characters")
    @Column(nullable = false, length = 160)
    private String institution;

    /** Starting year, e.g. 2022. */
    @NotNull(message = "Start year is required")
    @Min(value = 1950, message = "Start year must be 1950 or later")
    @Max(value = 2100, message = "Start year is not valid")
    @Column(nullable = false)
    private Integer startYear;

    /** Ending year, e.g. 2026 (or the expected year). */
    @NotNull(message = "End year is required")
    @Min(value = 1950, message = "End year must be 1950 or later")
    @Max(value = 2100, message = "End year is not valid")
    @Column(nullable = false)
    private Integer endYear;

    /** Free text so both "8.7 CGPA" and "91%" can be stored. */
    @Size(max = 30, message = "Result must not exceed 30 characters")
    @Column(name = "percentage_or_cgpa", length = 30)
    private String percentageOrCgpa;

    /** Short description shown under the timeline entry. */
    @Size(max = 600, message = "Description must not exceed 600 characters")
    @Column(length = 600)
    private String description;

    /** Lower number = shown first. */
    @Column(nullable = false)
    private int sortOrder = 0;

    // =====================================================================
    //  CONSTRUCTORS
    // =====================================================================

    public Education() {
    }

    public Education(String degree, String institution, Integer startYear, Integer endYear,
                     String percentageOrCgpa, String description, int sortOrder) {
        this.degree = degree;
        this.institution = institution;
        this.startYear = startYear;
        this.endYear = endYear;
        this.percentageOrCgpa = percentageOrCgpa;
        this.description = description;
        this.sortOrder = sortOrder;
    }

    /** "2022 - 2026" - convenience for the timeline header. */
    public String getYearRange() {
        return startYear + " - " + endYear;
    }

    // =====================================================================
    //  GETTERS / SETTERS
    // =====================================================================

    public Long getId() {
        return id;
    }

    public void setId(Long id) {
        this.id = id;
    }

    public String getDegree() {
        return degree;
    }

    public void setDegree(String degree) {
        this.degree = degree;
    }

    public String getInstitution() {
        return institution;
    }

    public void setInstitution(String institution) {
        this.institution = institution;
    }

    public Integer getStartYear() {
        return startYear;
    }

    public void setStartYear(Integer startYear) {
        this.startYear = startYear;
    }

    public Integer getEndYear() {
        return endYear;
    }

    public void setEndYear(Integer endYear) {
        this.endYear = endYear;
    }

    public String getPercentageOrCgpa() {
        return percentageOrCgpa;
    }

    public void setPercentageOrCgpa(String percentageOrCgpa) {
        this.percentageOrCgpa = percentageOrCgpa;
    }

    public String getDescription() {
        return description;
    }

    public void setDescription(String description) {
        this.description = description;
    }

    public int getSortOrder() {
        return sortOrder;
    }

    public void setSortOrder(int sortOrder) {
        this.sortOrder = sortOrder;
    }

    public AdminUser getUser() {
        return user;
    }

    public void setUser(AdminUser user) {
        this.user = user;
    }
}

```

---

## `portfolio-app/src/main/java/com/portfolio/entity/Experience.java`
<a id="portfolio-app-src-main-java-com-portfolio-entity-experiencejava"></a>

```java
package com.portfolio.entity;

import jakarta.persistence.Column;
import jakarta.persistence.Entity;
import jakarta.persistence.GeneratedValue;
import jakarta.persistence.GenerationType;
import jakarta.persistence.Id;
import jakarta.persistence.Table;
import jakarta.validation.constraints.NotBlank;
import jakarta.validation.constraints.Size;

import java.time.LocalDate;

/**
 * ============================================================================
 * ENTITY : Experience
 * TABLE  : experiences
 * ============================================================================
 * One row = one internship / job / volunteering role.
 * Dates are nullable so "Present" can be shown for a current role
 * (the view prints "Present" whenever endDate is null).
 * ============================================================================
 */
@Entity
@Table(name = "experiences")
public class Experience {

    @Id
    @GeneratedValue(strategy = GenerationType.IDENTITY)
    private Long id;

    @com.fasterxml.jackson.annotation.JsonIgnore
    @jakarta.persistence.ManyToOne(fetch = jakarta.persistence.FetchType.LAZY)
    @jakarta.persistence.JoinColumn(name = "user_id")
    private AdminUser user;

    /** e.g. "Java Developer Intern". */
    @NotBlank(message = "Position is required")
    @Size(max = 120, message = "Position must not exceed 120 characters")
    @Column(nullable = false, length = 120)
    private String position;

    /** e.g. "ABC Technologies Pvt. Ltd.". */
    @NotBlank(message = "Organization is required")
    @Size(max = 160, message = "Organization must not exceed 160 characters")
    @Column(nullable = false, length = 160)
    private String organization;

    @Column(name = "start_date")
    private LocalDate startDate;

    /** null = currently working here. */
    @Column(name = "end_date")
    private LocalDate endDate;

    /** Responsibilities - one bullet per line. */
    @Column(columnDefinition = "TEXT")
    private String description;

    /** Comma separated technologies used in this role. */
    @Size(max = 300, message = "Technologies must not exceed 300 characters")
    @Column(length = 300)
    private String technologies;

    /** Lower number = shown first. */
    @Column(nullable = false)
    private int sortOrder = 0;

    // =====================================================================
    //  CONSTRUCTORS
    // =====================================================================

    public Experience() {
    }

    public Experience(String position, String organization, LocalDate startDate, LocalDate endDate,
                      String description, String technologies, int sortOrder) {
        this.position = position;
        this.organization = organization;
        this.startDate = startDate;
        this.endDate = endDate;
        this.description = description;
        this.technologies = technologies;
        this.sortOrder = sortOrder;
    }

    // =====================================================================
    //  HELPER METHODS (used by Thymeleaf templates)
    // =====================================================================

    /** Responsibilities as a list, one entry per line entered by the admin. */
    public java.util.List<String> getResponsibilityList() {
        if (description == null || description.isBlank()) {
            return java.util.List.of();
        }
        String[] parts = description.split("\\r?\\n|;");
        java.util.List<String> list = new java.util.ArrayList<>();
        for (String part : parts) {
            String trimmed = part.trim().replaceAll("^[-*\u2022]\\s*", "");
            if (!trimmed.isEmpty()) {
                list.add(trimmed);
            }
        }
        return list;
    }

    /** Comma separated technologies as a list (for badges). */
    public java.util.List<String> getTechnologyList() {
        if (technologies == null || technologies.isBlank()) {
            return java.util.List.of();
        }
        String[] parts = technologies.split(",");
        java.util.List<String> list = new java.util.ArrayList<>();
        for (String part : parts) {
            String trimmed = part.trim();
            if (!trimmed.isEmpty()) {
                list.add(trimmed);
            }
        }
        return list;
    }

    /** "Jun 2024 - Present" style label. Null safe. */
    public String getDateRange() {
        java.time.format.DateTimeFormatter fmt =
                java.time.format.DateTimeFormatter.ofPattern("MMM yyyy");
        String start = (startDate == null) ? "" : startDate.format(fmt);
        String end = (endDate == null) ? "Present" : endDate.format(fmt);
        if (start.isEmpty()) {
            return end;
        }
        return start + " - " + end;
    }

    // =====================================================================
    //  GETTERS / SETTERS
    // =====================================================================

    public Long getId() {
        return id;
    }

    public void setId(Long id) {
        this.id = id;
    }

    public String getPosition() {
        return position;
    }

    public void setPosition(String position) {
        this.position = position;
    }

    public String getOrganization() {
        return organization;
    }

    public void setOrganization(String organization) {
        this.organization = organization;
    }

    public LocalDate getStartDate() {
        return startDate;
    }

    public void setStartDate(LocalDate startDate) {
        this.startDate = startDate;
    }

    public LocalDate getEndDate() {
        return endDate;
    }

    public void setEndDate(LocalDate endDate) {
        this.endDate = endDate;
    }

    public String getDescription() {
        return description;
    }

    public void setDescription(String description) {
        this.description = description;
    }

    public String getTechnologies() {
        return technologies;
    }

    public void setTechnologies(String technologies) {
        this.technologies = technologies;
    }

    public int getSortOrder() {
        return sortOrder;
    }

    public void setSortOrder(int sortOrder) {
        this.sortOrder = sortOrder;
    }

    public AdminUser getUser() {
        return user;
    }

    public void setUser(AdminUser user) {
        this.user = user;
    }
}

```

---

## `portfolio-app/src/main/java/com/portfolio/entity/Project.java`
<a id="portfolio-app-src-main-java-com-portfolio-entity-projectjava"></a>

```java
package com.portfolio.entity;

import jakarta.persistence.Column;
import jakarta.persistence.Entity;
import jakarta.persistence.EnumType;
import jakarta.persistence.Enumerated;
import jakarta.persistence.GeneratedValue;
import jakarta.persistence.GenerationType;
import jakarta.persistence.Id;
import jakarta.persistence.Table;
import jakarta.validation.constraints.Max;
import jakarta.validation.constraints.Min;
import jakarta.validation.constraints.NotBlank;
import jakarta.validation.constraints.NotNull;
import jakarta.validation.constraints.Size;

import java.time.LocalDateTime;

/**
 * ============================================================================
 * ENTITY : Project
 * TABLE  : projects
 * ============================================================================
 * Represents one portfolio project shown on the public "Projects" page and
 * managed (Create / Read / Update / Delete) from the admin panel.
 *
 * RELATIONSHIP
 *   Project has NO foreign key to other tables - it is an independent root
 *   entity. This keeps the schema simple, which is exactly what a portfolio
 *   needs (and is easy to explain in a viva).
 *
 * NOTE ON "features" AND "technologies"
 *   Both are stored as a single VARCHAR holding comma separated values,
 *   e.g. "Spring Boot, MySQL, Bootstrap".
 *   The helper method {@link #getTechnologyList()} splits them for the view,
 *   so the template can render a Bootstrap badge per technology.
 *   A normalised child table (project_technology) would be the "textbook"
 *   approach, but for a portfolio a delimited column is far simpler and the
 *   admin form stays a single text box.
 * ============================================================================
 */
@Entity
@Table(name = "projects")
public class Project {

    /** Primary key - auto incremented by MySQL. */
    @Id
    @GeneratedValue(strategy = GenerationType.IDENTITY)
    private Long id;

    @com.fasterxml.jackson.annotation.JsonIgnore
    @jakarta.persistence.ManyToOne(fetch = jakarta.persistence.FetchType.LAZY)
    @jakarta.persistence.JoinColumn(name = "user_id")
    private AdminUser user;

    /** Project title, e.g. "Library Management System". */
    @NotBlank(message = "Project title is required")
    @Size(max = 120, message = "Title must not exceed 120 characters")
    @Column(nullable = false, length = 120)
    private String title;

    /** Short description used on the project card. */
    @NotBlank(message = "Short description is required")
    @Size(max = 500, message = "Short description must not exceed 500 characters")
    @Column(nullable = false, length = 500)
    private String description;

    /** The problem this project solves - shown on the detail page. */
    @Size(max = 1000, message = "Problem statement must not exceed 1000 characters")
    @Column(length = 1000)
    private String problemStatement;

    /** Full feature list, one feature per line - shown on the detail page. */
    @Column(columnDefinition = "TEXT")
    private String features;

    /** Comma separated technologies, e.g. "Java, Spring Boot, MySQL". */
    @NotBlank(message = "At least one technology is required")
    @Size(max = 300, message = "Technologies must not exceed 300 characters")
    @Column(nullable = false, length = 300)
    private String technologies;

    /** GitHub repository link. */
    @Size(max = 300, message = "GitHub URL must not exceed 300 characters")
    @Column(length = 300)
    private String githubUrl;

    /** Live demo link. */
    @Size(max = 300, message = "Demo URL must not exceed 300 characters")
    @Column(length = 300)
    private String demoUrl;

    /** Path of the project cover image, e.g. "/uploads/abc123.png". */
    @Size(max = 300)
    @Column(length = 300)
    private String imageUrl;

    /**
     * Category used by the front-end filter buttons
     * (All / Java / Web / AI / Database / Other).
     */
    @NotNull(message = "Please choose a category")
    @Enumerated(EnumType.STRING)
    @Column(nullable = false, length = 30)
    private ProjectCategory category = ProjectCategory.JAVA;

    /** Whether the project is visible on the public website. */
    @Column(nullable = false)
    private boolean featured = true;

    /** Lower number = shown first. Editable from the admin panel. */
    @Column(nullable = false)
    private int sortOrder = 0;

    /** Set automatically by the service layer on insert. */
    @Column(name = "created_at", nullable = false, updatable = false)
    private LocalDateTime createdAt = LocalDateTime.now();

    // =====================================================================
    //  CONSTRUCTORS
    // =====================================================================

    /** No-arg constructor - REQUIRED by JPA / Hibernate. */
    public Project() {
    }

    /** Convenience constructor used by the sample-data seeder. */
    public Project(String title, String description, String problemStatement, String features,
                   String technologies, String githubUrl, String demoUrl, String imageUrl,
                   ProjectCategory category, boolean featured, int sortOrder) {
        this.title = title;
        this.description = description;
        this.problemStatement = problemStatement;
        this.features = features;
        this.technologies = technologies;
        this.githubUrl = githubUrl;
        this.demoUrl = demoUrl;
        this.imageUrl = imageUrl;
        this.category = category;
        this.featured = featured;
        this.sortOrder = sortOrder;
    }

    // =====================================================================
    //  HELPER METHODS (used by Thymeleaf templates)
    // =====================================================================

    /**
     * Splits the comma separated "technologies" column into a list so the
     * template can print one badge per technology.
     *
     * @return list of trimmed, non-empty technology names (never null)
     */
    public java.util.List<String> getTechnologyList() {
        return splitToList(this.technologies);
    }

    /**
     * Splits the "features" column. The admin enters one feature per line,
     * so we split on newlines but also accept "; " as a separator.
     *
     * @return list of trimmed, non-empty feature lines (never null)
     */
    public java.util.List<String> getFeatureList() {
        if (features == null || features.isBlank()) {
            return java.util.List.of();
        }
        String[] parts = features.split("\\r?\\n|;");
        java.util.List<String> list = new java.util.ArrayList<>();
        for (String part : parts) {
            String trimmed = part.trim().replaceAll("^[-*\u2022]\\s*", "");
            if (!trimmed.isEmpty()) {
                list.add(trimmed);
            }
        }
        return list;
    }

    /** Small shared utility: comma separated string -> clean list. */
    private static java.util.List<String> splitToList(String csv) {
        if (csv == null || csv.isBlank()) {
            return java.util.List.of();
        }
        String[] parts = csv.split(",");
        java.util.List<String> list = new java.util.ArrayList<>();
        for (String part : parts) {
            String trimmed = part.trim();
            if (!trimmed.isEmpty()) {
                list.add(trimmed);
            }
        }
        return list;
    }

    // =====================================================================
    //  GETTERS / SETTERS
    // =====================================================================

    public Long getId() {
        return id;
    }

    public void setId(Long id) {
        this.id = id;
    }

    public String getTitle() {
        return title;
    }

    public void setTitle(String title) {
        this.title = title;
    }

    public String getDescription() {
        return description;
    }

    public void setDescription(String description) {
        this.description = description;
    }

    public String getProblemStatement() {
        return problemStatement;
    }

    public void setProblemStatement(String problemStatement) {
        this.problemStatement = problemStatement;
    }

    public String getFeatures() {
        return features;
    }

    public void setFeatures(String features) {
        this.features = features;
    }

    public String getTechnologies() {
        return technologies;
    }

    public void setTechnologies(String technologies) {
        this.technologies = technologies;
    }

    public String getGithubUrl() {
        return githubUrl;
    }

    public void setGithubUrl(String githubUrl) {
        this.githubUrl = githubUrl;
    }

    public String getDemoUrl() {
        return demoUrl;
    }

    public void setDemoUrl(String demoUrl) {
        this.demoUrl = demoUrl;
    }

    public String getImageUrl() {
        return imageUrl;
    }

    public void setImageUrl(String imageUrl) {
        this.imageUrl = imageUrl;
    }

    public ProjectCategory getCategory() {
        return category;
    }

    public void setCategory(ProjectCategory category) {
        this.category = category;
    }

    public boolean isFeatured() {
        return featured;
    }

    public void setFeatured(boolean featured) {
        this.featured = featured;
    }

    public int getSortOrder() {
        return sortOrder;
    }

    public void setSortOrder(int sortOrder) {
        this.sortOrder = sortOrder;
    }

    public LocalDateTime getCreatedAt() {
        return createdAt;
    }

    public void setCreatedAt(LocalDateTime createdAt) {
        this.createdAt = createdAt;
    }

    public AdminUser getUser() {
        return user;
    }

    public void setUser(AdminUser user) {
        this.user = user;
    }
}

```

---

## `portfolio-app/src/main/java/com/portfolio/entity/ProjectCategory.java`
<a id="portfolio-app-src-main-java-com-portfolio-entity-projectcategoryjava"></a>

```java
package com.portfolio.entity;

/**
 * ============================================================================
 * ENUM : ProjectCategory
 * ============================================================================
 * Stored as a VARCHAR (see {@code @Enumerated(EnumType.STRING)} on the entity)
 * so the MySQL column contains readable values like "JAVA" instead of "0".
 *
 * These values drive the filter buttons on the public Projects page:
 *   All | Java | Web | AI | Database | Other
 * ============================================================================
 */
public enum ProjectCategory {

    JAVA("Java"),
    WEB("Web"),
    AI("AI / ML"),
    DATABASE("Database"),
    IOT("IoT"),
    OTHER("Other");

    /** Human readable label used in drop-downs and filter buttons. */
    private final String label;

    ProjectCategory(String label) {
        this.label = label;
    }

    public String getLabel() {
        return label;
    }
}

```

---

## `portfolio-app/src/main/java/com/portfolio/entity/SettingKey.java`
<a id="portfolio-app-src-main-java-com-portfolio-entity-settingkeyjava"></a>

```java
package com.portfolio.entity;

/**
 * ============================================================================
 * CONSTANTS : SettingKey
 * ============================================================================
 * Every key that can exist in the {@code site_settings} table, in one place.
 *
 * Why constants instead of typing "hero.name" everywhere?
 *   - a typo becomes a compile error instead of a silent null at runtime
 *   - you can see the whole list of profile fields at a glance
 *   - the seeder and the admin form both use the same values
 * ============================================================================
 */
public final class SettingKey {

    /** Not instantiable - this is only a container for constants. */
    private SettingKey() {
    }

    // ---------------- HERO / HOME ----------------
    public static final String HERO_NAME = "hero.name";
    public static final String HERO_TITLE = "hero.title";
    public static final String HERO_INTRO = "hero.intro";
    public static final String HERO_TYPING_WORDS = "hero.typingWords";
    public static final String PROFILE_IMAGE = "profile.image";
    public static final String RESUME_URL = "resume.url";

    // ---------------- ABOUT ----------------
    public static final String ABOUT_INTRO = "about.intro";
    public static final String ABOUT_OBJECTIVE = "about.objective";
    public static final String ABOUT_INTERESTS = "about.interests";
    public static final String ABOUT_DOB = "about.dob";
    public static final String ABOUT_EMAIL = "about.email";
    public static final String ABOUT_PHONE = "about.phone";
    public static final String ABOUT_LOCATION = "about.location";
    public static final String ABOUT_LANGUAGES = "about.languages";

    // ---------------- SOCIAL ----------------
    public static final String SOCIAL_GITHUB = "social.github";
    public static final String SOCIAL_LINKEDIN = "social.linkedin";
    public static final String SOCIAL_TWITTER = "social.twitter";
    public static final String SOCIAL_INSTAGRAM = "social.instagram";

    /**
     * SERVICES (the "What I Do" section) - one service per line in the format
     *     icon|title|description
     * e.g. "code|Java Development|Developing Java based applications"
     * Parsed into {@code ServiceItem} objects by {@code SiteSettingService}.
     */
    public static final String SERVICES = "services.list";
}

```

---

## `portfolio-app/src/main/java/com/portfolio/entity/SiteSetting.java`
<a id="portfolio-app-src-main-java-com-portfolio-entity-sitesettingjava"></a>

```java
package com.portfolio.entity;

import jakarta.persistence.Column;
import jakarta.persistence.Entity;
import jakarta.persistence.GeneratedValue;
import jakarta.persistence.GenerationType;
import jakarta.persistence.Id;
import jakarta.persistence.Table;

import java.time.LocalDateTime;

/**
 * ============================================================================
 * ENTITY : SiteSetting   (key / value table)
 * TABLE  : site_settings
 * ============================================================================
 * A portfolio has a handful of "profile" details that are not big enough to
 * deserve their own table: the name in the hero section, the typing line,
 * the career objective, the social links and so on.
 *
 * Storing them as key-value rows means:
 *   - the admin can edit every word on the home page from the browser
 *   - no schema change is needed when a new field is added later
 *
 * All keys used by the application are listed in {@code SettingKey}.
 * ============================================================================
 */
@Entity
@Table(name = "site_settings", uniqueConstraints = {
        @jakarta.persistence.UniqueConstraint(columnNames = {"user_id", "setting_key"})
})
public class SiteSetting {

    @Id
    @GeneratedValue(strategy = GenerationType.IDENTITY)
    private Long id;

    @com.fasterxml.jackson.annotation.JsonIgnore
    @jakarta.persistence.ManyToOne(fetch = jakarta.persistence.FetchType.LAZY)
    @jakarta.persistence.JoinColumn(name = "user_id")
    private AdminUser user;

    /** Setting key, e.g. "hero.name". */
    @Column(name = "setting_key", nullable = false, length = 60)
    private String key;

    /** Setting value. TEXT so long paragraphs (about me) fit. */
    @Column(name = "setting_value", columnDefinition = "TEXT")
    private String value;

    /** Human readable label shown in the admin form. */
    @Column(length = 120)
    private String label;

    @Column(name = "updated_at")
    private LocalDateTime updatedAt = LocalDateTime.now();

    // =====================================================================
    //  CONSTRUCTORS
    // =====================================================================

    public SiteSetting() {
    }

    public SiteSetting(String key, String value, String label) {
        this.key = key;
        this.value = value;
        this.label = label;
    }

    public SiteSetting(AdminUser user, String key, String value, String label) {
        this.user = user;
        this.key = key;
        this.value = value;
        this.label = label;
    }

    // =====================================================================
    //  GETTERS / SETTERS
    // =====================================================================

    public Long getId() {
        return id;
    }

    public void setId(Long id) {
        this.id = id;
    }

    public String getKey() {
        return key;
    }

    public void setKey(String key) {
        this.key = key;
    }

    public String getValue() {
        return value;
    }

    public void setValue(String value) {
        this.value = value;
    }

    public String getLabel() {
        return label;
    }

    public void setLabel(String label) {
        this.label = label;
    }

    public LocalDateTime getUpdatedAt() {
        return updatedAt;
    }

    public void setUpdatedAt(LocalDateTime updatedAt) {
        this.updatedAt = updatedAt;
    }

    public AdminUser getUser() {
        return user;
    }

    public void setUser(AdminUser user) {
        this.user = user;
    }
}

```

---

## `portfolio-app/src/main/java/com/portfolio/entity/Skill.java`
<a id="portfolio-app-src-main-java-com-portfolio-entity-skilljava"></a>

```java
package com.portfolio.entity;

import jakarta.persistence.Column;
import jakarta.persistence.Entity;
import jakarta.persistence.GeneratedValue;
import jakarta.persistence.GenerationType;
import jakarta.persistence.Id;
import jakarta.persistence.Table;
import jakarta.validation.constraints.Max;
import jakarta.validation.constraints.Min;
import jakarta.validation.constraints.NotBlank;
import jakarta.validation.constraints.NotNull;
import jakarta.validation.constraints.Size;

/**
 * ============================================================================
 * ENTITY : Skill
 * TABLE  : skills
 * ============================================================================
 * One row = one skill with a category and a proficiency percentage.
 * The public Skills page groups these rows by category and renders a
 * Bootstrap progress bar per skill.
 * ============================================================================
 */
@Entity
@Table(name = "skills")
public class Skill {

    @Id
    @GeneratedValue(strategy = GenerationType.IDENTITY)
    private Long id;

    @com.fasterxml.jackson.annotation.JsonIgnore
    @jakarta.persistence.ManyToOne(fetch = jakarta.persistence.FetchType.LAZY)
    @jakarta.persistence.JoinColumn(name = "user_id")
    private AdminUser user;

    /** Skill name, e.g. "Java", "Spring Boot", "MySQL". */
    @NotBlank(message = "Skill name is required")
    @Size(max = 60, message = "Skill name must not exceed 60 characters")
    @Column(nullable = false, length = 60)
    private String name;

    /** Category - drives the grouping on the public page. */
    @NotBlank(message = "Category is required")
    @Size(max = 60, message = "Category must not exceed 60 characters")
    @Column(nullable = false, length = 60)
    private String category;

    /**
     * Proficiency 0..100 (width of the progress bar).
     * {@code @Min} / {@code @Max} give backend validation, and the HTML form
     * adds the same limits client side.
     */
    @NotNull(message = "Proficiency is required")
    @Min(value = 0, message = "Proficiency must be at least 0")
    @Max(value = 100, message = "Proficiency must not exceed 100")
    @Column(nullable = false)
    private Integer proficiency;

    /** Lower number = shown first inside its category. */
    @Column(nullable = false)
    private int sortOrder = 0;

    // =====================================================================
    //  CONSTRUCTORS
    // =====================================================================

    public Skill() {
    }

    public Skill(String name, String category, Integer proficiency, int sortOrder) {
        this.name = name;
        this.category = category;
        this.proficiency = proficiency;
        this.sortOrder = sortOrder;
    }

    /**
     * Bootstrap progress-bar colour class based on the proficiency value.
     * Used by Thymeleaf so bars are coloured without extra JavaScript.
     *
     * @return one of "bg-success", "bg-info", "bg-warning", "bg-danger"
     */
    public String getBarClass() {
        if (proficiency == null) {
            return "bg-secondary";
        }
        if (proficiency >= 85) {
            return "bg-success";
        }
        if (proficiency >= 70) {
            return "bg-info";
        }
        if (proficiency >= 50) {
            return "bg-warning";
        }
        return "bg-danger";
    }

    // =====================================================================
    //  GETTERS / SETTERS
    // =====================================================================

    public Long getId() {
        return id;
    }

    public void setId(Long id) {
        this.id = id;
    }

    public String getName() {
        return name;
    }

    public void setName(String name) {
        this.name = name;
    }

    public String getCategory() {
        return category;
    }

    public void setCategory(String category) {
        this.category = category;
    }

    public Integer getProficiency() {
        return proficiency;
    }

    public void setProficiency(Integer proficiency) {
        this.proficiency = proficiency;
    }

    public int getSortOrder() {
        return sortOrder;
    }

    public void setSortOrder(int sortOrder) {
        this.sortOrder = sortOrder;
    }

    public AdminUser getUser() {
        return user;
    }

    public void setUser(AdminUser user) {
        this.user = user;
    }
}

```

---

# 4. Data Transfer Objects (DTOs)

## `portfolio-app/src/main/java/com/portfolio/dto/ChangePasswordForm.java`
<a id="portfolio-app-src-main-java-com-portfolio-dto-changepasswordformjava"></a>

```java
package com.portfolio.dto;

import jakarta.validation.constraints.AssertTrue;
import jakarta.validation.constraints.NotBlank;
import jakarta.validation.constraints.Size;

/**
 * ============================================================================
 * DTO : ChangePasswordForm
 * ============================================================================
 * A form-backing object for the "Change Password" screen.
 *
 * It is NOT a JPA entity: it exists only to carry three strings from the
 * browser to the controller, and it is never written to the database.
 *
 * The {@code @AssertTrue} method is a neat trick - it turns a custom rule
 * ("the two new passwords must match") into an ordinary bean-validation error
 * that Thymeleaf can display under the field.
 * ============================================================================
 */
public class ChangePasswordForm {

    @NotBlank(message = "Please enter your current password")
    private String currentPassword;

    @NotBlank(message = "Please enter a new password")
    @Size(min = 8, max = 60, message = "The new password must be between 8 and 60 characters")
    private String newPassword;

    @NotBlank(message = "Please confirm the new password")
    private String confirmPassword;

    public ChangePasswordForm() {
    }

    /**
     * Custom validation rule.
     * The method name must follow the pattern isXxx() / getXxx() and return a
     * boolean for {@code @AssertTrue} to pick it up.
     */
    @AssertTrue(message = "The new password and the confirmation do not match")
    public boolean isPasswordMatching() {
        if (newPassword == null || confirmPassword == null) {
            return false;
        }
        return newPassword.equals(confirmPassword);
    }

    // =====================================================================
    //  GETTERS / SETTERS
    // =====================================================================

    public String getCurrentPassword() {
        return currentPassword;
    }

    public void setCurrentPassword(String currentPassword) {
        this.currentPassword = currentPassword;
    }

    public String getNewPassword() {
        return newPassword;
    }

    public void setNewPassword(String newPassword) {
        this.newPassword = newPassword;
    }

    public String getConfirmPassword() {
        return confirmPassword;
    }

    public void setConfirmPassword(String confirmPassword) {
        this.confirmPassword = confirmPassword;
    }
}

```

---

## `portfolio-app/src/main/java/com/portfolio/dto/DashboardStats.java`
<a id="portfolio-app-src-main-java-com-portfolio-dto-dashboardstatsjava"></a>

```java
package com.portfolio.dto;

/**
 * ============================================================================
 * DTO : DashboardStats
 * ============================================================================
 * A Java {@code record} - the modern (Java 16+) way to write an immutable
 * data holder. The compiler generates the constructor, the accessors
 * (totalProjects(), totalSkills(), ...), equals(), hashCode() and toString().
 *
 * Used to send every dashboard number to the view in one object instead of
 * adding eight separate model attributes.
 * ============================================================================
 */
public record DashboardStats(
        long totalProjects,
        long totalSkills,
        long totalCertifications,
        long totalAchievements,
        long totalExperiences,
        long totalEducations,
        long totalMessages,
        long unreadMessages
) {
    /** Projects + skills + certifications + ... - "everything in the database". */
    public long totalRecords() {
        return totalProjects + totalSkills + totalCertifications
                + totalAchievements + totalExperiences + totalEducations + totalMessages;
    }
}

```

---

## `portfolio-app/src/main/java/com/portfolio/dto/RegisterForm.java`
<a id="portfolio-app-src-main-java-com-portfolio-dto-registerformjava"></a>

```java
package com.portfolio.dto;

import jakarta.validation.constraints.Email;
import jakarta.validation.constraints.NotBlank;
import jakarta.validation.constraints.Pattern;
import jakarta.validation.constraints.Size;

/**
 * ============================================================================
 * DTO : RegisterForm
 * ============================================================================
 * Captures user inputs from the /register sign-up form.
 * ============================================================================
 */
public class RegisterForm {

    @NotBlank(message = "Full Name is required")
    @Size(min = 2, max = 80, message = "Full Name must be between 2 and 80 characters")
    private String fullName;

    @NotBlank(message = "Email is required")
    @Email(message = "Please enter a valid email address")
    @Size(max = 100, message = "Email cannot exceed 100 characters")
    private String email;

    @NotBlank(message = "Username is required")
    @Size(min = 3, max = 40, message = "Username must be between 3 and 40 characters")
    @Pattern(regexp = "^[a-zA-Z0-9._-]+$", message = "Username can only contain letters, numbers, dots, and hyphens")
    private String username;

    @Size(max = 120, message = "Headline cannot exceed 120 characters")
    private String headline;

    @NotBlank(message = "Password is required")
    @Size(min = 6, max = 100, message = "Password must be at least 6 characters long")
    private String password;

    @NotBlank(message = "Please confirm your password")
    private String confirmPassword;

    public RegisterForm() {
    }

    public String getFullName() {
        return fullName;
    }

    public void setFullName(String fullName) {
        this.fullName = fullName;
    }

    public String getEmail() {
        return email;
    }

    public void setEmail(String email) {
        this.email = email;
    }

    public String getUsername() {
        return username;
    }

    public void setUsername(String username) {
        this.username = username;
    }

    public String getHeadline() {
        return headline;
    }

    public void setHeadline(String headline) {
        this.headline = headline;
    }

    public String getPassword() {
        return password;
    }

    public void setPassword(String password) {
        this.password = password;
    }

    public String getConfirmPassword() {
        return confirmPassword;
    }

    public void setConfirmPassword(String confirmPassword) {
        this.confirmPassword = confirmPassword;
    }

    public boolean isPasswordMatching() {
        return password != null && password.equals(confirmPassword);
    }
}

```

---

## `portfolio-app/src/main/java/com/portfolio/dto/ServiceItem.java`
<a id="portfolio-app-src-main-java-com-portfolio-dto-serviceitemjava"></a>

```java
package com.portfolio.dto;

/**
 * ============================================================================
 * DTO : ServiceItem
 * ============================================================================
 * A DTO (Data Transfer Object) is a plain object used to carry data to the
 * view. It is not a JPA entity - it has no table behind it.
 *
 * One ServiceItem = one card in the "What I Do" section:
 *   icon        -> which Bootstrap icon to draw
 *   title       -> "Java Development"
 *   description -> "Developing Java based applications"
 *
 * It is built from a single line of the {@code services.list} setting, which
 * uses the format: icon|title|description
 * ============================================================================
 */
public record ServiceItem(String icon, String title, String description) {

    /**
     * Parses one setting line into a ServiceItem.
     * Returns {@code null} for blank or malformed lines so the caller can
     * simply skip them without crashing the whole page.
     *
     * @param line a line like "code|Java Development|Developing Java apps"
     * @return the parsed item, or null when the line is unusable
     */
    public static ServiceItem fromLine(String line) {
        if (line == null || line.isBlank()) {
            return null;
        }
        String[] parts = line.split("\\|", -1);
        if (parts.length < 2) {
            return null;
        }
        String icon = parts[0].trim();
        String title = parts[1].trim();
        String description = parts.length > 2 ? parts[2].trim() : "";
        if (icon.isEmpty()) {
            icon = "star";
        }
        if (title.isEmpty()) {
            return null;
        }
        return new ServiceItem(icon, title, description);
    }
}

```

---

# 5. Spring Data JPA Repositories

## `portfolio-app/src/main/java/com/portfolio/repository/AchievementRepository.java`
<a id="portfolio-app-src-main-java-com-portfolio-repository-achievementrepositoryjava"></a>

```java
package com.portfolio.repository;

import com.portfolio.entity.Achievement;
import org.springframework.data.jpa.repository.JpaRepository;
import org.springframework.data.jpa.repository.Query;
import org.springframework.stereotype.Repository;

import java.util.List;

/**
 * ============================================================================
 * REPOSITORY : AchievementRepository
 * ============================================================================
 */
@Repository
public interface AchievementRepository extends JpaRepository<Achievement, Long> {

    /** Newest achievement first. */
    List<Achievement> findAllByOrderByAchievementDateDescSortOrderAsc();

    @Query("SELECT a FROM Achievement a WHERE LOWER(a.title) LIKE LOWER(CONCAT('%', :keyword, '%')) "
            + "OR LOWER(a.organization) LIKE LOWER(CONCAT('%', :keyword, '%')) "
            + "OR LOWER(a.category) LIKE LOWER(CONCAT('%', :keyword, '%')) "
            + "ORDER BY a.achievementDate DESC")
    List<Achievement> searchByKeyword(String keyword);

    /** Hackathon count for the "About" statistics. */
    long countByCategoryIgnoreCase(String category);

    // =====================================================================
    //  USER-SCOPED QUERIES
    // =====================================================================

    List<Achievement> findByUserOrderByAchievementDateDescSortOrderAsc(com.portfolio.entity.AdminUser user);

    long countByUser(com.portfolio.entity.AdminUser user);

    long countByUserAndCategoryIgnoreCase(com.portfolio.entity.AdminUser user, String category);

    java.util.Optional<Achievement> findByIdAndUser(Long id, com.portfolio.entity.AdminUser user);

    @Query("SELECT a FROM Achievement a WHERE a.user = :user AND (LOWER(a.title) LIKE LOWER(CONCAT('%', :keyword, '%')) "
            + "OR LOWER(a.organization) LIKE LOWER(CONCAT('%', :keyword, '%')) "
            + "OR LOWER(a.category) LIKE LOWER(CONCAT('%', :keyword, '%'))) "
            + "ORDER BY a.achievementDate DESC")
    List<Achievement> searchByUserAndKeyword(@org.springframework.data.repository.query.Param("user") com.portfolio.entity.AdminUser user, @org.springframework.data.repository.query.Param("keyword") String keyword);
}

```

---

## `portfolio-app/src/main/java/com/portfolio/repository/AdminUserRepository.java`
<a id="portfolio-app-src-main-java-com-portfolio-repository-adminuserrepositoryjava"></a>

```java
package com.portfolio.repository;

import com.portfolio.entity.AdminUser;
import org.springframework.data.jpa.repository.JpaRepository;
import org.springframework.stereotype.Repository;

import java.util.Optional;

/**
 * ============================================================================
 * REPOSITORY : AdminUserRepository
 * ============================================================================
 * Used by {@code CustomUserDetailsService} during login, and by the
 * Settings screen when the admin changes the password.
 * ============================================================================
 */
@Repository
public interface AdminUserRepository extends JpaRepository<AdminUser, Long> {

    /** Spring Security loads the account by username during authentication. */
    Optional<AdminUser> findByUsername(String username);

    /** Spring Security loads account by email. */
    Optional<AdminUser> findByEmail(String email);

    /** Spring Security can load by either username or email. */
    Optional<AdminUser> findByUsernameOrEmail(String username, String email);

    /** Used to make sure a new username is not already taken. */
    boolean existsByUsername(String username);

    /** Used to make sure a new email is not already taken. */
    boolean existsByEmail(String email);

    /** List all active users for the Explore page. */
    java.util.List<AdminUser> findByEnabledTrueOrderByCreatedAtDesc();
}

```

---

## `portfolio-app/src/main/java/com/portfolio/repository/CertificationRepository.java`
<a id="portfolio-app-src-main-java-com-portfolio-repository-certificationrepositoryjava"></a>

```java
package com.portfolio.repository;

import com.portfolio.entity.Certification;
import org.springframework.data.jpa.repository.JpaRepository;
import org.springframework.data.jpa.repository.Query;
import org.springframework.stereotype.Repository;

import java.util.List;

/**
 * ============================================================================
 * REPOSITORY : CertificationRepository
 * ============================================================================
 */
@Repository
public interface CertificationRepository extends JpaRepository<Certification, Long> {

    /** Newest certificate first. */
    List<Certification> findAllByOrderByIssueDateDescSortOrderAsc();

    @Query("SELECT c FROM Certification c WHERE LOWER(c.title) LIKE LOWER(CONCAT('%', :keyword, '%')) "
            + "OR LOWER(c.issuer) LIKE LOWER(CONCAT('%', :keyword, '%')) "
            + "ORDER BY c.issueDate DESC")
    List<Certification> searchByKeyword(String keyword);

    // =====================================================================
    //  USER-SCOPED QUERIES
    // =====================================================================

    List<Certification> findByUserOrderByIssueDateDescSortOrderAsc(com.portfolio.entity.AdminUser user);

    long countByUser(com.portfolio.entity.AdminUser user);

    java.util.Optional<Certification> findByIdAndUser(Long id, com.portfolio.entity.AdminUser user);

    @Query("SELECT c FROM Certification c WHERE c.user = :user AND (LOWER(c.title) LIKE LOWER(CONCAT('%', :keyword, '%')) "
            + "OR LOWER(c.issuer) LIKE LOWER(CONCAT('%', :keyword, '%'))) "
            + "ORDER BY c.issueDate DESC")
    List<Certification> searchByUserAndKeyword(@org.springframework.data.repository.query.Param("user") com.portfolio.entity.AdminUser user, @org.springframework.data.repository.query.Param("keyword") String keyword);
}

```

---

## `portfolio-app/src/main/java/com/portfolio/repository/ContactMessageRepository.java`
<a id="portfolio-app-src-main-java-com-portfolio-repository-contactmessagerepositoryjava"></a>

```java
package com.portfolio.repository;

import com.portfolio.entity.ContactMessage;
import org.springframework.data.jpa.repository.JpaRepository;
import org.springframework.data.jpa.repository.Query;
import org.springframework.stereotype.Repository;

import java.util.List;

/**
 * ============================================================================
 * REPOSITORY : ContactMessageRepository
 * ============================================================================
 */
@Repository
public interface ContactMessageRepository extends JpaRepository<ContactMessage, Long> {

    /** Newest message first. */
    List<ContactMessage> findAllByOrderByCreatedAtDesc();

    /** Unread only - powers the red badge in the admin sidebar. */
    List<ContactMessage> findByReadStatusFalseOrderByCreatedAtDesc();

    long countByReadStatusFalse();

    /** Admin search box. */
    @Query("SELECT m FROM ContactMessage m WHERE LOWER(m.name) LIKE LOWER(CONCAT('%', :keyword, '%')) "
            + "OR LOWER(m.email) LIKE LOWER(CONCAT('%', :keyword, '%')) "
            + "OR LOWER(m.subject) LIKE LOWER(CONCAT('%', :keyword, '%')) "
            + "OR LOWER(m.message) LIKE LOWER(CONCAT('%', :keyword, '%')) "
            + "ORDER BY m.createdAt DESC")
    List<ContactMessage> searchByKeyword(String keyword);

    // =====================================================================
    //  RECIPIENT-SCOPED QUERIES
    // =====================================================================

    List<ContactMessage> findByRecipientOrderByCreatedAtDesc(com.portfolio.entity.AdminUser recipient);

    List<ContactMessage> findByRecipientAndReadStatusFalseOrderByCreatedAtDesc(com.portfolio.entity.AdminUser recipient);

    long countByRecipientAndReadStatusFalse(com.portfolio.entity.AdminUser recipient);

    long countByRecipient(com.portfolio.entity.AdminUser recipient);

    java.util.Optional<ContactMessage> findByIdAndRecipient(Long id, com.portfolio.entity.AdminUser recipient);

    @Query("SELECT m FROM ContactMessage m WHERE m.recipient = :recipient AND (LOWER(m.name) LIKE LOWER(CONCAT('%', :keyword, '%')) "
            + "OR LOWER(m.email) LIKE LOWER(CONCAT('%', :keyword, '%')) "
            + "OR LOWER(m.subject) LIKE LOWER(CONCAT('%', :keyword, '%')) "
            + "OR LOWER(m.message) LIKE LOWER(CONCAT('%', :keyword, '%'))) "
            + "ORDER BY m.createdAt DESC")
    List<ContactMessage> searchByRecipientAndKeyword(@org.springframework.data.repository.query.Param("recipient") com.portfolio.entity.AdminUser recipient, @org.springframework.data.repository.query.Param("keyword") String keyword);
}

```

---

## `portfolio-app/src/main/java/com/portfolio/repository/EducationRepository.java`
<a id="portfolio-app-src-main-java-com-portfolio-repository-educationrepositoryjava"></a>

```java
package com.portfolio.repository;

import com.portfolio.entity.Education;
import org.springframework.data.jpa.repository.JpaRepository;
import org.springframework.data.jpa.repository.Query;
import org.springframework.stereotype.Repository;

import java.util.List;

/**
 * ============================================================================
 * REPOSITORY : EducationRepository
 * ============================================================================
 */
@Repository
public interface EducationRepository extends JpaRepository<Education, Long> {

    /** Newest qualification first (descending end year). */
    List<Education> findAllByOrderByEndYearDescSortOrderAsc();

    @Query("SELECT e FROM Education e WHERE LOWER(e.degree) LIKE LOWER(CONCAT('%', :keyword, '%')) "
            + "OR LOWER(e.institution) LIKE LOWER(CONCAT('%', :keyword, '%')) "
            + "ORDER BY e.endYear DESC")
    List<Education> searchByKeyword(String keyword);

    // =====================================================================
    //  USER-SCOPED QUERIES
    // =====================================================================

    List<Education> findByUserOrderByEndYearDescSortOrderAsc(com.portfolio.entity.AdminUser user);

    long countByUser(com.portfolio.entity.AdminUser user);

    java.util.Optional<Education> findByIdAndUser(Long id, com.portfolio.entity.AdminUser user);

    @Query("SELECT e FROM Education e WHERE e.user = :user AND (LOWER(e.degree) LIKE LOWER(CONCAT('%', :keyword, '%')) "
            + "OR LOWER(e.institution) LIKE LOWER(CONCAT('%', :keyword, '%'))) "
            + "ORDER BY e.endYear DESC")
    List<Education> searchByUserAndKeyword(@org.springframework.data.repository.query.Param("user") com.portfolio.entity.AdminUser user, @org.springframework.data.repository.query.Param("keyword") String keyword);
}

```

---

## `portfolio-app/src/main/java/com/portfolio/repository/ExperienceRepository.java`
<a id="portfolio-app-src-main-java-com-portfolio-repository-experiencerepositoryjava"></a>

```java
package com.portfolio.repository;

import com.portfolio.entity.Experience;
import org.springframework.data.jpa.repository.JpaRepository;
import org.springframework.data.jpa.repository.Query;
import org.springframework.stereotype.Repository;

import java.util.List;

/**
 * ============================================================================
 * REPOSITORY : ExperienceRepository
 * ============================================================================
 */
@Repository
public interface ExperienceRepository extends JpaRepository<Experience, Long> {

    /** Newest role first; a current role (null end date) sorts to the top. */
    List<Experience> findAllByOrderByStartDateDescSortOrderAsc();

    @Query("SELECT e FROM Experience e WHERE LOWER(e.position) LIKE LOWER(CONCAT('%', :keyword, '%')) "
            + "OR LOWER(e.organization) LIKE LOWER(CONCAT('%', :keyword, '%')) "
            + "ORDER BY e.startDate DESC")
    List<Experience> searchByKeyword(String keyword);

    // =====================================================================
    //  USER-SCOPED QUERIES
    // =====================================================================

    List<Experience> findByUserOrderByStartDateDescSortOrderAsc(com.portfolio.entity.AdminUser user);

    long countByUser(com.portfolio.entity.AdminUser user);

    java.util.Optional<Experience> findByIdAndUser(Long id, com.portfolio.entity.AdminUser user);

    @Query("SELECT e FROM Experience e WHERE e.user = :user AND (LOWER(e.position) LIKE LOWER(CONCAT('%', :keyword, '%')) "
            + "OR LOWER(e.organization) LIKE LOWER(CONCAT('%', :keyword, '%'))) "
            + "ORDER BY e.startDate DESC")
    List<Experience> searchByUserAndKeyword(@org.springframework.data.repository.query.Param("user") com.portfolio.entity.AdminUser user, @org.springframework.data.repository.query.Param("keyword") String keyword);
}

```

---

## `portfolio-app/src/main/java/com/portfolio/repository/ProjectRepository.java`
<a id="portfolio-app-src-main-java-com-portfolio-repository-projectrepositoryjava"></a>

```java
package com.portfolio.repository;

import com.portfolio.entity.Project;
import com.portfolio.entity.ProjectCategory;
import org.springframework.data.jpa.repository.JpaRepository;
import org.springframework.data.jpa.repository.Query;
import org.springframework.data.repository.query.Param;
import org.springframework.stereotype.Repository;

import java.util.List;

/**
 * ============================================================================
 * REPOSITORY : ProjectRepository
 * ============================================================================
 * Extending {@code JpaRepository<Project, Long>} gives us for free:
 *   save(), findById(), findAll(), deleteById(), count(), existsById() ...
 *
 * The methods below are "derived queries": Spring Data reads the METHOD NAME
 * and writes the SQL for us at start-up - no SQL to maintain.
 * ============================================================================
 */
@Repository
public interface ProjectRepository extends JpaRepository<Project, Long> {

    /** Public website ordering: sortOrder first, then newest first. */
    List<Project> findAllByOrderBySortOrderAscIdDesc();

    /** Only the projects marked "featured" (visible on the public site). */
    List<Project> findByFeaturedTrueOrderBySortOrderAscIdDesc();

    /** Filter buttons on the public page (Java / Web / AI / Database / Other). */
    List<Project> findByFeaturedTrueAndCategoryOrderBySortOrderAscIdDesc(ProjectCategory category);

    /** Admin list page filter by category. */
    List<Project> findByCategoryOrderBySortOrderAscIdDesc(ProjectCategory category);

    /**
     * Search box on the admin project list.
     * LOWER(...) on both sides makes the search case insensitive.
     */
    @Query("SELECT p FROM Project p WHERE "
            + "LOWER(p.title) LIKE LOWER(CONCAT('%', :keyword, '%')) OR "
            + "LOWER(p.technologies) LIKE LOWER(CONCAT('%', :keyword, '%')) OR "
            + "LOWER(p.description) LIKE LOWER(CONCAT('%', :keyword, '%')) "
            + "ORDER BY p.sortOrder ASC, p.id DESC")
    List<Project> searchByKeyword(@Param("keyword") String keyword);

    /** Count of visible projects - used for the hero statistics. */
    long countByFeaturedTrue();

    // =====================================================================
    //  USER-SCOPED QUERIES
    // =====================================================================

    List<Project> findByUserOrderBySortOrderAscIdDesc(com.portfolio.entity.AdminUser user);

    List<Project> findByUserAndFeaturedTrueOrderBySortOrderAscIdDesc(com.portfolio.entity.AdminUser user);

    List<Project> findByUserAndCategoryOrderBySortOrderAscIdDesc(com.portfolio.entity.AdminUser user, ProjectCategory category);

    List<Project> findByUserAndFeaturedTrueAndCategoryOrderBySortOrderAscIdDesc(com.portfolio.entity.AdminUser user, ProjectCategory category);

    java.util.Optional<Project> findByIdAndUser(Long id, com.portfolio.entity.AdminUser user);

    long countByUser(com.portfolio.entity.AdminUser user);

    long countByUserAndFeaturedTrue(com.portfolio.entity.AdminUser user);

    @Query("SELECT p FROM Project p WHERE p.user = :user AND ("
            + "LOWER(p.title) LIKE LOWER(CONCAT('%', :keyword, '%')) OR "
            + "LOWER(p.technologies) LIKE LOWER(CONCAT('%', :keyword, '%')) OR "
            + "LOWER(p.description) LIKE LOWER(CONCAT('%', :keyword, '%'))) "
            + "ORDER BY p.sortOrder ASC, p.id DESC")
    List<Project> searchByUserAndKeyword(@Param("user") com.portfolio.entity.AdminUser user, @Param("keyword") String keyword);
}

```

---

## `portfolio-app/src/main/java/com/portfolio/repository/SiteSettingRepository.java`
<a id="portfolio-app-src-main-java-com-portfolio-repository-sitesettingrepositoryjava"></a>

```java
package com.portfolio.repository;

import com.portfolio.entity.SiteSetting;
import org.springframework.data.jpa.repository.JpaRepository;
import org.springframework.stereotype.Repository;

import java.util.Optional;

/**
 * ============================================================================
 * REPOSITORY : SiteSettingRepository
 * ============================================================================
 */
@Repository
public interface SiteSettingRepository extends JpaRepository<SiteSetting, Long> {

    Optional<SiteSetting> findByKey(String key);

    Optional<SiteSetting> findFirstByKey(String key);

    Optional<SiteSetting> findByUserIsNullAndKey(String key);

    Optional<SiteSetting> findByUserAndKey(com.portfolio.entity.AdminUser user, String key);

    java.util.List<SiteSetting> findByUser(com.portfolio.entity.AdminUser user);

    java.util.List<SiteSetting> findByUserIsNull();
}

```

---

## `portfolio-app/src/main/java/com/portfolio/repository/SkillRepository.java`
<a id="portfolio-app-src-main-java-com-portfolio-repository-skillrepositoryjava"></a>

```java
package com.portfolio.repository;

import com.portfolio.entity.Skill;
import org.springframework.data.jpa.repository.JpaRepository;
import org.springframework.data.jpa.repository.Query;
import org.springframework.stereotype.Repository;

import java.util.List;

/**
 * ============================================================================
 * REPOSITORY : SkillRepository
 * ============================================================================
 */
@Repository
public interface SkillRepository extends JpaRepository<Skill, Long> {

    List<Skill> findAllByOrderByCategoryAscSortOrderAscNameAsc();

    /** Distinct category names, used to fill the admin drop-down. */
    @Query("SELECT DISTINCT s.category FROM Skill s ORDER BY s.category ASC")
    List<String> findAllCategories();

    /** Admin search box. */
    @Query("SELECT s FROM Skill s WHERE LOWER(s.name) LIKE LOWER(CONCAT('%', :keyword, '%')) "
            + "OR LOWER(s.category) LIKE LOWER(CONCAT('%', :keyword, '%')) "
            + "ORDER BY s.category ASC, s.sortOrder ASC")
    List<Skill> searchByKeyword(String keyword);

    // =====================================================================
    //  USER-SCOPED QUERIES
    // =====================================================================

    List<Skill> findByUserOrderByCategoryAscSortOrderAscNameAsc(com.portfolio.entity.AdminUser user);

    List<Skill> findByUser(com.portfolio.entity.AdminUser user);

    long countByUser(com.portfolio.entity.AdminUser user);

    java.util.Optional<Skill> findByIdAndUser(Long id, com.portfolio.entity.AdminUser user);

    @Query("SELECT DISTINCT s.category FROM Skill s WHERE s.user = :user ORDER BY s.category ASC")
    List<String> findCategoriesByUser(@org.springframework.data.repository.query.Param("user") com.portfolio.entity.AdminUser user);

    @Query("SELECT s FROM Skill s WHERE s.user = :user AND (LOWER(s.name) LIKE LOWER(CONCAT('%', :keyword, '%')) "
            + "OR LOWER(s.category) LIKE LOWER(CONCAT('%', :keyword, '%'))) "
            + "ORDER BY s.category ASC, s.sortOrder ASC")
    List<Skill> searchByUserAndKeyword(@org.springframework.data.repository.query.Param("user") com.portfolio.entity.AdminUser user, @org.springframework.data.repository.query.Param("keyword") String keyword);
}

```

---

# 6. Service Layer (Interfaces & Implementations)

## `portfolio-app/src/main/java/com/portfolio/service/AchievementService.java`
<a id="portfolio-app-src-main-java-com-portfolio-service-achievementservicejava"></a>

```java
package com.portfolio.service;

import com.portfolio.entity.Achievement;
import com.portfolio.exception.ResourceNotFoundException;
import com.portfolio.repository.AchievementRepository;
import org.springframework.stereotype.Service;
import org.springframework.transaction.annotation.Transactional;

import java.util.List;

/**
 * ============================================================================
 * SERVICE : AchievementService
 * ============================================================================
 */
@Service
@Transactional
public class AchievementService {

    private final AchievementRepository achievementRepository;

    public AchievementService(AchievementRepository achievementRepository) {
        this.achievementRepository = achievementRepository;
    }

    @Transactional(readOnly = true)
    public List<Achievement> getAll() {
        return achievementRepository.findAllByOrderByAchievementDateDescSortOrderAsc();
    }

    @Transactional(readOnly = true)
    public List<Achievement> search(String keyword) {
        if (keyword == null || keyword.isBlank()) {
            return getAll();
        }
        return achievementRepository.searchByKeyword(keyword.trim());
    }

    @Transactional(readOnly = true)
    public Achievement getById(Long id) {
        return achievementRepository.findById(id)
                .orElseThrow(() -> new ResourceNotFoundException("Achievement not found with id: " + id));
    }

    public Achievement save(Achievement achievement) {
        if (achievement.getCategory() == null || achievement.getCategory().isBlank()) {
            achievement.setCategory("Achievement");
        }
        return achievementRepository.save(achievement);
    }

    public void delete(Long id) {
        if (!achievementRepository.existsById(id)) {
            throw new ResourceNotFoundException("Achievement not found with id: " + id);
        }
        achievementRepository.deleteById(id);
    }

    @Transactional(readOnly = true)
    public long countAll() {
        return achievementRepository.count();
    }

    /** Number of hackathon entries - shown in the About statistics. */
    @Transactional(readOnly = true)
    public long countHackathons() {
        return achievementRepository.countByCategoryIgnoreCase("Hackathon");
    }

    // =====================================================================
    //  USER-SCOPED METHODS
    // =====================================================================

    @Transactional(readOnly = true)
    public List<Achievement> getAll(com.portfolio.entity.AdminUser user) {
        if (user == null) {
            return getAll();
        }
        return achievementRepository.findByUserOrderByAchievementDateDescSortOrderAsc(user);
    }

    @Transactional(readOnly = true)
    public List<Achievement> search(com.portfolio.entity.AdminUser user, String keyword) {
        if (user == null) {
            return search(keyword);
        }
        if (keyword == null || keyword.isBlank()) {
            return getAll(user);
        }
        return achievementRepository.searchByUserAndKeyword(user, keyword.trim());
    }

    @Transactional(readOnly = true)
    public Achievement getByIdAndUser(Long id, com.portfolio.entity.AdminUser user) {
        if (user == null) {
            return getById(id);
        }
        return achievementRepository.findByIdAndUser(id, user)
                .orElseThrow(() -> new ResourceNotFoundException("Achievement not found with id: " + id));
    }

    @Transactional(readOnly = true)
    public long countAll(com.portfolio.entity.AdminUser user) {
        if (user == null) {
            return countAll();
        }
        return achievementRepository.countByUser(user);
    }

    @Transactional(readOnly = true)
    public long countHackathons(com.portfolio.entity.AdminUser user) {
        if (user == null) {
            return countHackathons();
        }
        return achievementRepository.countByUserAndCategoryIgnoreCase(user, "Hackathon");
    }
}

```

---

## `portfolio-app/src/main/java/com/portfolio/service/CertificationService.java`
<a id="portfolio-app-src-main-java-com-portfolio-service-certificationservicejava"></a>

```java
package com.portfolio.service;

import com.portfolio.entity.Certification;
import com.portfolio.exception.ResourceNotFoundException;
import com.portfolio.repository.CertificationRepository;
import org.springframework.stereotype.Service;
import org.springframework.transaction.annotation.Transactional;

import java.util.List;

/**
 * ============================================================================
 * SERVICE : CertificationService
 * ============================================================================
 */
@Service
@Transactional
public class CertificationService {

    private final CertificationRepository certificationRepository;

    public CertificationService(CertificationRepository certificationRepository) {
        this.certificationRepository = certificationRepository;
    }

    @Transactional(readOnly = true)
    public List<Certification> getAll() {
        return certificationRepository.findAllByOrderByIssueDateDescSortOrderAsc();
    }

    @Transactional(readOnly = true)
    public List<Certification> search(String keyword) {
        if (keyword == null || keyword.isBlank()) {
            return getAll();
        }
        return certificationRepository.searchByKeyword(keyword.trim());
    }

    @Transactional(readOnly = true)
    public Certification getById(Long id) {
        return certificationRepository.findById(id)
                .orElseThrow(() -> new ResourceNotFoundException("Certification not found with id: " + id));
    }

    /** Keeps the previously uploaded image when the form is saved without a new file. */
    public Certification save(Certification certification) {
        if (certification.getId() != null
                && (certification.getImageUrl() == null || certification.getImageUrl().isBlank())) {
            certification.setImageUrl(getById(certification.getId()).getImageUrl());
        }
        return certificationRepository.save(certification);
    }

    public void delete(Long id) {
        if (!certificationRepository.existsById(id)) {
            throw new ResourceNotFoundException("Certification not found with id: " + id);
        }
        certificationRepository.deleteById(id);
    }

    @Transactional(readOnly = true)
    public long countAll() {
        return certificationRepository.count();
    }

    // =====================================================================
    //  USER-SCOPED METHODS
    // =====================================================================

    @Transactional(readOnly = true)
    public List<Certification> getAll(com.portfolio.entity.AdminUser user) {
        if (user == null) {
            return getAll();
        }
        return certificationRepository.findByUserOrderByIssueDateDescSortOrderAsc(user);
    }

    @Transactional(readOnly = true)
    public List<Certification> search(com.portfolio.entity.AdminUser user, String keyword) {
        if (user == null) {
            return search(keyword);
        }
        if (keyword == null || keyword.isBlank()) {
            return getAll(user);
        }
        return certificationRepository.searchByUserAndKeyword(user, keyword.trim());
    }

    @Transactional(readOnly = true)
    public Certification getByIdAndUser(Long id, com.portfolio.entity.AdminUser user) {
        if (user == null) {
            return getById(id);
        }
        return certificationRepository.findByIdAndUser(id, user)
                .orElseThrow(() -> new ResourceNotFoundException("Certification not found with id: " + id));
    }

    @Transactional(readOnly = true)
    public long countAll(com.portfolio.entity.AdminUser user) {
        if (user == null) {
            return countAll();
        }
        return certificationRepository.countByUser(user);
    }
}

```

---

## `portfolio-app/src/main/java/com/portfolio/service/ContactMessageService.java`
<a id="portfolio-app-src-main-java-com-portfolio-service-contactmessageservicejava"></a>

```java
package com.portfolio.service;

import com.portfolio.entity.ContactMessage;

import java.util.List;

/**
 * ============================================================================
 * SERVICE INTERFACE : ContactMessageService
 * ============================================================================
 */
public interface ContactMessageService {

    List<ContactMessage> getAllMessages();

    List<ContactMessage> searchMessages(String keyword);

    ContactMessage getMessageById(Long id);

    /** Called when a visitor submits the public contact form. */
    ContactMessage saveMessage(ContactMessage message);

    /** Toggles / sets the read flag from the admin panel. */
    ContactMessage markAsRead(Long id, boolean read);

    void deleteMessage(Long id);

    long countAll();

    long countUnread();

    // =====================================================================
    //  RECIPIENT-SCOPED METHODS
    // =====================================================================

    List<ContactMessage> getAllMessages(com.portfolio.entity.AdminUser recipient);

    List<ContactMessage> searchMessages(com.portfolio.entity.AdminUser recipient, String keyword);

    ContactMessage getMessageByIdAndRecipient(Long id, com.portfolio.entity.AdminUser recipient);

    long countAll(com.portfolio.entity.AdminUser recipient);

    long countUnread(com.portfolio.entity.AdminUser recipient);
}

```

---

## `portfolio-app/src/main/java/com/portfolio/service/ContactMessageServiceImpl.java`
<a id="portfolio-app-src-main-java-com-portfolio-service-contactmessageserviceimpljava"></a>

```java
package com.portfolio.service;

import com.portfolio.entity.ContactMessage;
import com.portfolio.exception.ResourceNotFoundException;
import com.portfolio.repository.ContactMessageRepository;
import org.springframework.stereotype.Service;
import org.springframework.transaction.annotation.Transactional;

import java.time.LocalDateTime;
import java.util.List;

/**
 * ============================================================================
 * SERVICE IMPLEMENTATION : ContactMessageServiceImpl
 * ============================================================================
 */
@Service
@Transactional
public class ContactMessageServiceImpl implements ContactMessageService {

    private final ContactMessageRepository messageRepository;

    public ContactMessageServiceImpl(ContactMessageRepository messageRepository) {
        this.messageRepository = messageRepository;
    }

    @Override
    @Transactional(readOnly = true)
    public List<ContactMessage> getAllMessages() {
        return messageRepository.findAllByOrderByCreatedAtDesc();
    }

    @Override
    @Transactional(readOnly = true)
    public List<ContactMessage> searchMessages(String keyword) {
        if (keyword == null || keyword.isBlank()) {
            return getAllMessages();
        }
        return messageRepository.searchByKeyword(keyword.trim());
    }

    @Override
    @Transactional(readOnly = true)
    public ContactMessage getMessageById(Long id) {
        return messageRepository.findById(id)
                .orElseThrow(() -> new ResourceNotFoundException("Message not found with id: " + id));
    }

    /**
     * Stores a message coming from the public contact form.
     *
     * The values are trimmed and the received timestamp is replaced by the
     * server clock - never trust a date sent by the browser.
     */
    @Override
    public ContactMessage saveMessage(ContactMessage message) {
        message.setName(trim(message.getName()));
        message.setEmail(trim(message.getEmail()));
        message.setSubject(trim(message.getSubject()));
        message.setMessage(trim(message.getMessage()));
        message.setCreatedAt(LocalDateTime.now());
        message.setReadStatus(false);
        return messageRepository.save(message);
    }

    @Override
    public ContactMessage markAsRead(Long id, boolean read) {
        ContactMessage message = getMessageById(id);
        message.setReadStatus(read);
        return messageRepository.save(message);
    }

    @Override
    public void deleteMessage(Long id) {
        if (!messageRepository.existsById(id)) {
            throw new ResourceNotFoundException("Message not found with id: " + id);
        }
        messageRepository.deleteById(id);
    }

    @Override
    @Transactional(readOnly = true)
    public long countAll() {
        return messageRepository.count();
    }

    @Override
    @Transactional(readOnly = true)
    public long countUnread() {
        return messageRepository.countByReadStatusFalse();
    }

    // =====================================================================
    //  RECIPIENT-SCOPED IMPLEMENTATIONS
    // =====================================================================

    @Override
    @Transactional(readOnly = true)
    public List<ContactMessage> getAllMessages(com.portfolio.entity.AdminUser recipient) {
        if (recipient == null) {
            return getAllMessages();
        }
        return messageRepository.findByRecipientOrderByCreatedAtDesc(recipient);
    }

    @Override
    @Transactional(readOnly = true)
    public List<ContactMessage> searchMessages(com.portfolio.entity.AdminUser recipient, String keyword) {
        if (recipient == null) {
            return searchMessages(keyword);
        }
        if (keyword == null || keyword.isBlank()) {
            return getAllMessages(recipient);
        }
        return messageRepository.searchByRecipientAndKeyword(recipient, keyword.trim());
    }

    @Override
    @Transactional(readOnly = true)
    public ContactMessage getMessageByIdAndRecipient(Long id, com.portfolio.entity.AdminUser recipient) {
        if (recipient == null) {
            return getMessageById(id);
        }
        return messageRepository.findByIdAndRecipient(id, recipient)
                .orElseThrow(() -> new ResourceNotFoundException("Message not found with id: " + id));
    }

    @Override
    @Transactional(readOnly = true)
    public long countAll(com.portfolio.entity.AdminUser recipient) {
        if (recipient == null) {
            return countAll();
        }
        return messageRepository.countByRecipient(recipient);
    }

    @Override
    @Transactional(readOnly = true)
    public long countUnread(com.portfolio.entity.AdminUser recipient) {
        if (recipient == null) {
            return countUnread();
        }
        return messageRepository.countByRecipientAndReadStatusFalse(recipient);
    }

    /** Trims a string and turns null into "" so the entity never holds nulls. */
    private String trim(String value) {
        return value == null ? "" : value.trim();
    }
}

```

---

## `portfolio-app/src/main/java/com/portfolio/service/DashboardService.java`
<a id="portfolio-app-src-main-java-com-portfolio-service-dashboardservicejava"></a>

```java
package com.portfolio.service;

import com.portfolio.dto.DashboardStats;
import org.springframework.stereotype.Service;
import org.springframework.transaction.annotation.Transactional;

/**
 * ============================================================================
 * SERVICE : DashboardService
 * ============================================================================
 * Collects the counters shown on the admin dashboard and in the hero
 * statistics. It has no repository of its own - it simply asks the other
 * services, which keeps each service responsible for one table only.
 * ============================================================================
 */
@Service
@Transactional(readOnly = true)
public class DashboardService {

    private final ProjectService projectService;
    private final SkillService skillService;
    private final CertificationService certificationService;
    private final AchievementService achievementService;
    private final ExperienceService experienceService;
    private final EducationService educationService;
    private final ContactMessageService contactMessageService;

    public DashboardService(ProjectService projectService,
                            SkillService skillService,
                            CertificationService certificationService,
                            AchievementService achievementService,
                            ExperienceService experienceService,
                            EducationService educationService,
                            ContactMessageService contactMessageService) {
        this.projectService = projectService;
        this.skillService = skillService;
        this.certificationService = certificationService;
        this.achievementService = achievementService;
        this.experienceService = experienceService;
        this.educationService = educationService;
        this.contactMessageService = contactMessageService;
    }

    /** All counters in one object - one line of controller code. */
    public DashboardStats getStats() {
        return getStats(null);
    }

    public DashboardStats getStats(com.portfolio.entity.AdminUser user) {
        if (user == null) {
            return new DashboardStats(
                    projectService.countAll(),
                    skillService.countAll(),
                    certificationService.countAll(),
                    achievementService.countAll(),
                    experienceService.countAll(),
                    educationService.countAll(),
                    contactMessageService.countAll(),
                    contactMessageService.countUnread()
            );
        }
        return new DashboardStats(
                projectService.countAll(user),
                skillService.countAll(user),
                certificationService.countAll(user),
                achievementService.countAll(user),
                experienceService.countAll(user),
                educationService.countAll(user),
                contactMessageService.countAll(user),
                contactMessageService.countUnread(user)
        );
    }

    /** Unread message count - shown as the red badge in the admin sidebar. */
    public long getUnreadMessageCount() {
        return contactMessageService.countUnread();
    }

    public long getUnreadMessageCount(com.portfolio.entity.AdminUser user) {
        if (user == null) {
            return getUnreadMessageCount();
        }
        return contactMessageService.countUnread(user);
    }
}

```

---

## `portfolio-app/src/main/java/com/portfolio/service/EducationService.java`
<a id="portfolio-app-src-main-java-com-portfolio-service-educationservicejava"></a>

```java
package com.portfolio.service;

import com.portfolio.entity.Education;
import com.portfolio.exception.ResourceNotFoundException;
import com.portfolio.repository.EducationRepository;
import org.springframework.stereotype.Service;
import org.springframework.transaction.annotation.Transactional;

import java.util.List;

/**
 * ============================================================================
 * SERVICE : EducationService
 * ============================================================================
 * A single {@code @Service} class (no separate interface) because this
 * service has exactly one implementation and no extra business rules.
 * The heavier services (Project, Skill, ContactMessage) use the
 * interface + Impl pattern to show how it is done properly.
 * ============================================================================
 */
@Service
@Transactional
public class EducationService {

    private final EducationRepository educationRepository;

    public EducationService(EducationRepository educationRepository) {
        this.educationRepository = educationRepository;
    }

    @Transactional(readOnly = true)
    public List<Education> getAll() {
        return educationRepository.findAllByOrderByEndYearDescSortOrderAsc();
    }

    @Transactional(readOnly = true)
    public List<Education> search(String keyword) {
        if (keyword == null || keyword.isBlank()) {
            return getAll();
        }
        return educationRepository.searchByKeyword(keyword.trim());
    }

    @Transactional(readOnly = true)
    public Education getById(Long id) {
        return educationRepository.findById(id)
                .orElseThrow(() -> new ResourceNotFoundException("Education entry not found with id: " + id));
    }

    /** Saves after checking that the year range makes sense. */
    public Education save(Education education) {
        if (education.getStartYear() != null && education.getEndYear() != null
                && education.getEndYear() < education.getStartYear()) {
            throw new IllegalArgumentException("End year cannot be earlier than the start year");
        }
        return educationRepository.save(education);
    }

    public void delete(Long id) {
        if (!educationRepository.existsById(id)) {
            throw new ResourceNotFoundException("Education entry not found with id: " + id);
        }
        educationRepository.deleteById(id);
    }

    @Transactional(readOnly = true)
    public long countAll() {
        return educationRepository.count();
    }

    // =====================================================================
    //  USER-SCOPED METHODS
    // =====================================================================

    @Transactional(readOnly = true)
    public List<Education> getAll(com.portfolio.entity.AdminUser user) {
        if (user == null) {
            return getAll();
        }
        return educationRepository.findByUserOrderByEndYearDescSortOrderAsc(user);
    }

    @Transactional(readOnly = true)
    public List<Education> search(com.portfolio.entity.AdminUser user, String keyword) {
        if (user == null) {
            return search(keyword);
        }
        if (keyword == null || keyword.isBlank()) {
            return getAll(user);
        }
        return educationRepository.searchByUserAndKeyword(user, keyword.trim());
    }

    @Transactional(readOnly = true)
    public Education getByIdAndUser(Long id, com.portfolio.entity.AdminUser user) {
        if (user == null) {
            return getById(id);
        }
        return educationRepository.findByIdAndUser(id, user)
                .orElseThrow(() -> new ResourceNotFoundException("Education entry not found with id: " + id));
    }

    @Transactional(readOnly = true)
    public long countAll(com.portfolio.entity.AdminUser user) {
        if (user == null) {
            return countAll();
        }
        return educationRepository.countByUser(user);
    }
}

```

---

## `portfolio-app/src/main/java/com/portfolio/service/ExperienceService.java`
<a id="portfolio-app-src-main-java-com-portfolio-service-experienceservicejava"></a>

```java
package com.portfolio.service;

import com.portfolio.entity.Experience;
import com.portfolio.exception.ResourceNotFoundException;
import com.portfolio.repository.ExperienceRepository;
import org.springframework.stereotype.Service;
import org.springframework.transaction.annotation.Transactional;

import java.util.List;

/**
 * ============================================================================
 * SERVICE : ExperienceService
 * ============================================================================
 */
@Service
@Transactional
public class ExperienceService {

    private final ExperienceRepository experienceRepository;

    public ExperienceService(ExperienceRepository experienceRepository) {
        this.experienceRepository = experienceRepository;
    }

    @Transactional(readOnly = true)
    public List<Experience> getAll() {
        return experienceRepository.findAllByOrderByStartDateDescSortOrderAsc();
    }

    @Transactional(readOnly = true)
    public List<Experience> search(String keyword) {
        if (keyword == null || keyword.isBlank()) {
            return getAll();
        }
        return experienceRepository.searchByKeyword(keyword.trim());
    }

    @Transactional(readOnly = true)
    public Experience getById(Long id) {
        return experienceRepository.findById(id)
                .orElseThrow(() -> new ResourceNotFoundException("Experience entry not found with id: " + id));
    }

    public Experience save(Experience experience) {
        if (experience.getStartDate() != null && experience.getEndDate() != null
                && experience.getEndDate().isBefore(experience.getStartDate())) {
            throw new IllegalArgumentException("End date cannot be earlier than the start date");
        }
        return experienceRepository.save(experience);
    }

    public void delete(Long id) {
        if (!experienceRepository.existsById(id)) {
            throw new ResourceNotFoundException("Experience entry not found with id: " + id);
        }
        experienceRepository.deleteById(id);
    }

    @Transactional(readOnly = true)
    public long countAll() {
        return experienceRepository.count();
    }

    // =====================================================================
    //  USER-SCOPED METHODS
    // =====================================================================

    @Transactional(readOnly = true)
    public List<Experience> getAll(com.portfolio.entity.AdminUser user) {
        if (user == null) {
            return getAll();
        }
        return experienceRepository.findByUserOrderByStartDateDescSortOrderAsc(user);
    }

    @Transactional(readOnly = true)
    public List<Experience> search(com.portfolio.entity.AdminUser user, String keyword) {
        if (user == null) {
            return search(keyword);
        }
        if (keyword == null || keyword.isBlank()) {
            return getAll(user);
        }
        return experienceRepository.searchByUserAndKeyword(user, keyword.trim());
    }

    @Transactional(readOnly = true)
    public Experience getByIdAndUser(Long id, com.portfolio.entity.AdminUser user) {
        if (user == null) {
            return getById(id);
        }
        return experienceRepository.findByIdAndUser(id, user)
                .orElseThrow(() -> new ResourceNotFoundException("Experience entry not found with id: " + id));
    }

    @Transactional(readOnly = true)
    public long countAll(com.portfolio.entity.AdminUser user) {
        if (user == null) {
            return countAll();
        }
        return experienceRepository.countByUser(user);
    }
}

```

---

## `portfolio-app/src/main/java/com/portfolio/service/FileStorageService.java`
<a id="portfolio-app-src-main-java-com-portfolio-service-filestorageservicejava"></a>

```java
package com.portfolio.service;

import org.springframework.beans.factory.annotation.Value;
import org.springframework.stereotype.Service;
import org.springframework.web.multipart.MultipartFile;

import java.io.IOException;
import java.nio.file.Files;
import java.nio.file.Path;
import java.nio.file.Paths;
import java.nio.file.StandardCopyOption;
import java.util.Locale;
import java.util.Set;
import java.util.UUID;

/**
 * ============================================================================
 * SERVICE : FileStorageService
 * ============================================================================
 * Handles the image / PDF uploads made from the admin panel.
 *
 * WHERE THE FILES GO
 *   Files are written to the folder given by the property
 *   {@code app.upload.dir} (default: ./uploads, i.e. next to the project).
 *   The folder is exposed to the browser at /uploads/** by WebConfig, so a
 *   stored file appears at http://localhost:8080/uploads/xyz.png
 *
 *   Storing uploads OUTSIDE src/main/resources is deliberate: everything in
 *   target/classes is wiped on every rebuild, which would delete the images.
 *
 * SECURITY
 *   - only the extensions in ALLOWED_EXTENSIONS are accepted
 *   - the original file name is replaced by a random UUID, so a visitor can
 *     never overwrite an existing file or smuggle a path like "../../x.php"
 * ============================================================================
 */
@Service
public class FileStorageService {

    /** Extensions the admin is allowed to upload. */
    private static final Set<String> ALLOWED_EXTENSIONS =
            Set.of("jpg", "jpeg", "png", "gif", "webp", "svg", "pdf");

    /** Hard limit - 5 MB. Also configured in application.properties. */
    private static final long MAX_SIZE_BYTES = 5L * 1024 * 1024;

    private final Path uploadLocation;

    /**
     * {@code @Value} injects a property from application.properties into the
     * constructor. The upload folder is created at start-up if missing.
     */
    public FileStorageService(@Value("${app.upload.dir:./uploads}") String uploadDir) {
        this.uploadLocation = Paths.get(uploadDir).toAbsolutePath().normalize();
        try {
            Files.createDirectories(this.uploadLocation);
        } catch (IOException ex) {
            throw new IllegalStateException(
                    "Could not create the upload directory: " + uploadLocation, ex);
        }
    }

    /**
     * Saves one uploaded file and returns the public URL to store in the
     * database (for example "/uploads/3f2a...-photo.png").
     *
     * @param file the uploaded file from the multipart form
     * @return the URL path, or {@code null} when no file was chosen
     */
    public String store(MultipartFile file) {
        if (file == null || file.isEmpty()) {
            return null;
        }
        if (file.getSize() > MAX_SIZE_BYTES) {
            throw new IllegalArgumentException("File is too large. Maximum allowed size is 5 MB.");
        }

        String extension = extensionOf(file.getOriginalFilename());
        if (!ALLOWED_EXTENSIONS.contains(extension)) {
            throw new IllegalArgumentException(
                    "Only these file types are allowed: " + String.join(", ", ALLOWED_EXTENSIONS));
        }

        // Random name + original extension, e.g. "9b1c...-certificate.pdf"
        String fileName = UUID.randomUUID() + "-" + sanitize(file.getOriginalFilename());

        try {
            Path target = this.uploadLocation.resolve(fileName).normalize();

            // Path traversal guard: the resolved path must stay inside the
            // upload folder. Cheap insurance, worth mentioning in a viva.
            if (!target.startsWith(this.uploadLocation)) {
                throw new IllegalArgumentException("Invalid file path.");
            }

            Files.copy(file.getInputStream(), target, StandardCopyOption.REPLACE_EXISTING);
        } catch (IOException ex) {
            throw new IllegalStateException("Failed to store the file: " + fileName, ex);
        }

        return "/uploads/" + fileName;
    }

    /**
     * Deletes a previously uploaded file. Missing files are ignored, because a
     * record must still be deletable after someone removed the file by hand.
     */
    public void delete(String url) {
        if (url == null || !url.startsWith("/uploads/")) {
            return;
        }
        try {
            String fileName = url.substring("/uploads/".length());
            if (fileName.contains("/") || fileName.contains("\\")) {
                return;
            }
            Files.deleteIfExists(this.uploadLocation.resolve(fileName));
        } catch (IOException ignored) {
            // Not fatal - the database row is what matters.
        }
    }

    /** Lower-case extension without the dot; "" when there is none. */
    private String extensionOf(String originalFilename) {
        if (originalFilename == null) {
            return "";
        }
        int dot = originalFilename.lastIndexOf('.');
        if (dot < 0 || dot == originalFilename.length() - 1) {
            return "";
        }
        return originalFilename.substring(dot + 1).toLowerCase(Locale.ROOT);
    }

    /** Keeps letters, digits, dot, dash and underscore; strips everything else. */
    private String sanitize(String originalFilename) {
        if (originalFilename == null) {
            return "file";
        }
        String cleaned = originalFilename.replaceAll("[^a-zA-Z0-9._-]", "");
        return cleaned.isBlank() ? "file" : cleaned;
    }
}

```

---

## `portfolio-app/src/main/java/com/portfolio/service/ProjectService.java`
<a id="portfolio-app-src-main-java-com-portfolio-service-projectservicejava"></a>

```java
package com.portfolio.service;

import com.portfolio.entity.Project;
import com.portfolio.entity.ProjectCategory;

import java.util.List;

/**
 * ============================================================================
 * SERVICE INTERFACE : ProjectService
 * ============================================================================
 * The controller talks to THIS interface, never to the repository directly.
 *
 *      Controller  ->  Service (interface)  ->  ServiceImpl  ->  Repository  ->  MySQL
 *
 * Benefits (easy to explain in a viva):
 *   - the controller does not know how data is stored
 *   - business rules (validation, ordering, image handling) live in one place
 *   - the implementation can be swapped or mocked in unit tests
 * ============================================================================
 */
public interface ProjectService {

    /** All projects, admin ordering. */
    List<Project> getAllProjects();

    /** All projects, optionally filtered by category (admin list page). */
    List<Project> getAllProjects(ProjectCategory category);

    /** Keyword search used by the admin list page. */
    List<Project> searchProjects(String keyword);

    /** Only the projects visible on the public website. */
    List<Project> getPublicProjects();

    /** Public projects filtered by the category buttons. */
    List<Project> getPublicProjectsByCategory(ProjectCategory category);

    /** One project by id. */
    Project getProjectById(Long id);

    /** Create or update (Spring Data decides from the id). */
    Project saveProject(Project project);

    void deleteProject(Long id);

    long countAll();

    long countPublic();

    /** Distinct categories present in the data - for the filter buttons. */
    List<ProjectCategory> getAvailableCategories();

    // =====================================================================
    //  USER-SCOPED METHODS
    // =====================================================================

    List<Project> getAllProjects(com.portfolio.entity.AdminUser user, ProjectCategory category);

    List<Project> searchProjects(com.portfolio.entity.AdminUser user, String keyword);

    List<Project> getPublicProjects(com.portfolio.entity.AdminUser user);

    List<Project> getPublicProjectsByCategory(com.portfolio.entity.AdminUser user, ProjectCategory category);

    Project getProjectByIdAndUser(Long id, com.portfolio.entity.AdminUser user);

    long countAll(com.portfolio.entity.AdminUser user);

    long countPublic(com.portfolio.entity.AdminUser user);

    List<ProjectCategory> getAvailableCategories(com.portfolio.entity.AdminUser user);
}

```

---

## `portfolio-app/src/main/java/com/portfolio/service/ProjectServiceImpl.java`
<a id="portfolio-app-src-main-java-com-portfolio-service-projectserviceimpljava"></a>

```java
package com.portfolio.service;

import com.portfolio.entity.Project;
import com.portfolio.entity.ProjectCategory;
import com.portfolio.exception.ResourceNotFoundException;
import com.portfolio.repository.ProjectRepository;
import org.springframework.stereotype.Service;
import org.springframework.transaction.annotation.Transactional;

import java.time.LocalDateTime;
import java.util.ArrayList;
import java.util.List;
import java.util.stream.Collectors;

/**
 * ============================================================================
 * SERVICE IMPLEMENTATION : ProjectServiceImpl
 * ============================================================================
 * {@code @Service} registers this class as a Spring bean, so the controller
 * can receive it through its constructor (constructor injection).
 *
 * {@code @Transactional} opens one database transaction per call, so a method
 * either fully succeeds or is rolled back completely.
 * ============================================================================
 */
@Service
@Transactional
public class ProjectServiceImpl implements ProjectService {

    private final ProjectRepository projectRepository;

    /**
     * CONSTRUCTOR INJECTION
     * The repository is passed in by Spring. There is exactly one way to build
     * this object, which makes the dependency obvious and the class testable.
     */
    public ProjectServiceImpl(ProjectRepository projectRepository) {
        this.projectRepository = projectRepository;
    }

    @Override
    @Transactional(readOnly = true)
    public List<Project> getAllProjects() {
        return projectRepository.findAllByOrderBySortOrderAscIdDesc();
    }

    @Override
    @Transactional(readOnly = true)
    public List<Project> getAllProjects(ProjectCategory category) {
        if (category == null) {
            return getAllProjects();
        }
        return projectRepository.findByCategoryOrderBySortOrderAscIdDesc(category);
    }

    @Override
    @Transactional(readOnly = true)
    public List<Project> searchProjects(String keyword) {
        if (keyword == null || keyword.isBlank()) {
            return getAllProjects();
        }
        return projectRepository.searchByKeyword(keyword.trim());
    }

    @Override
    @Transactional(readOnly = true)
    public List<Project> getPublicProjects() {
        return projectRepository.findByFeaturedTrueOrderBySortOrderAscIdDesc();
    }

    @Override
    @Transactional(readOnly = true)
    public List<Project> getPublicProjectsByCategory(ProjectCategory category) {
        if (category == null) {
            return getPublicProjects();
        }
        return projectRepository.findByFeaturedTrueAndCategoryOrderBySortOrderAscIdDesc(category);
    }

    @Override
    @Transactional(readOnly = true)
    public Project getProjectById(Long id) {
        return projectRepository.findById(id)
                .orElseThrow(() -> new ResourceNotFoundException("Project not found with id: " + id));
    }

    /**
     * Saves a project. On insert we stamp {@code createdAt}; on update we keep
     * the original value so the "added on" date stays truthful.
     */
    @Override
    public Project saveProject(Project project) {
        if (project.getId() != null) {
            Project existing = getProjectById(project.getId());
            project.setCreatedAt(existing.getCreatedAt());
            // Keep the stored image when the admin submits the form without
            // uploading a new file (the form has no image field on edit).
            if (project.getImageUrl() == null || project.getImageUrl().isBlank()) {
                project.setImageUrl(existing.getImageUrl());
            }
        } else if (project.getCreatedAt() == null) {
            project.setCreatedAt(LocalDateTime.now());
        }
        return projectRepository.save(project);
    }

    @Override
    public void deleteProject(Long id) {
        if (!projectRepository.existsById(id)) {
            throw new ResourceNotFoundException("Project not found with id: " + id);
        }
        projectRepository.deleteById(id);
    }

    @Override
    @Transactional(readOnly = true)
    public long countAll() {
        return projectRepository.count();
    }

    @Override
    @Transactional(readOnly = true)
    public long countPublic() {
        return projectRepository.countByFeaturedTrue();
    }

    @Override
    @Transactional(readOnly = true)
    public List<ProjectCategory> getAvailableCategories() {
        List<ProjectCategory> used = projectRepository.findAll().stream()
                .map(Project::getCategory)
                .distinct()
                .collect(Collectors.toList());

        // Always show every filter button, even for categories that have no
        // project yet. Categories that DO have projects are listed first.
        List<ProjectCategory> ordered = new ArrayList<>(used);
        for (ProjectCategory category : ProjectCategory.values()) {
            if (!ordered.contains(category)) {
                ordered.add(category);
            }
        }
        return ordered;
    }

    // =====================================================================
    //  USER-SCOPED IMPLEMENTATIONS
    // =====================================================================

    @Override
    @Transactional(readOnly = true)
    public List<Project> getAllProjects(com.portfolio.entity.AdminUser user, ProjectCategory category) {
        if (user == null) {
            return getAllProjects(category);
        }
        if (category == null) {
            return projectRepository.findByUserOrderBySortOrderAscIdDesc(user);
        }
        return projectRepository.findByUserAndCategoryOrderBySortOrderAscIdDesc(user, category);
    }

    @Override
    @Transactional(readOnly = true)
    public List<Project> searchProjects(com.portfolio.entity.AdminUser user, String keyword) {
        if (user == null) {
            return searchProjects(keyword);
        }
        if (keyword == null || keyword.isBlank()) {
            return getAllProjects(user, null);
        }
        return projectRepository.searchByUserAndKeyword(user, keyword.trim());
    }

    @Override
    @Transactional(readOnly = true)
    public List<Project> getPublicProjects(com.portfolio.entity.AdminUser user) {
        if (user == null) {
            return getPublicProjects();
        }
        return projectRepository.findByUserAndFeaturedTrueOrderBySortOrderAscIdDesc(user);
    }

    @Override
    @Transactional(readOnly = true)
    public List<Project> getPublicProjectsByCategory(com.portfolio.entity.AdminUser user, ProjectCategory category) {
        if (user == null) {
            return getPublicProjectsByCategory(category);
        }
        if (category == null) {
            return getPublicProjects(user);
        }
        return projectRepository.findByUserAndFeaturedTrueAndCategoryOrderBySortOrderAscIdDesc(user, category);
    }

    @Override
    @Transactional(readOnly = true)
    public Project getProjectByIdAndUser(Long id, com.portfolio.entity.AdminUser user) {
        if (user == null) {
            return getProjectById(id);
        }
        return projectRepository.findByIdAndUser(id, user)
                .orElseThrow(() -> new ResourceNotFoundException("Project not found with id: " + id));
    }

    @Override
    @Transactional(readOnly = true)
    public long countAll(com.portfolio.entity.AdminUser user) {
        if (user == null) {
            return countAll();
        }
        return projectRepository.countByUser(user);
    }

    @Override
    @Transactional(readOnly = true)
    public long countPublic(com.portfolio.entity.AdminUser user) {
        if (user == null) {
            return countPublic();
        }
        return projectRepository.countByUserAndFeaturedTrue(user);
    }

    @Override
    @Transactional(readOnly = true)
    public List<ProjectCategory> getAvailableCategories(com.portfolio.entity.AdminUser user) {
        if (user == null) {
            return getAvailableCategories();
        }
        List<ProjectCategory> used = projectRepository.findByUserOrderBySortOrderAscIdDesc(user).stream()
                .map(Project::getCategory)
                .distinct()
                .collect(Collectors.toList());
        List<ProjectCategory> ordered = new ArrayList<>(used);
        for (ProjectCategory category : ProjectCategory.values()) {
            if (!ordered.contains(category)) {
                ordered.add(category);
            }
        }
        return ordered;
    }
}

```

---

## `portfolio-app/src/main/java/com/portfolio/service/SiteSettingService.java`
<a id="portfolio-app-src-main-java-com-portfolio-service-sitesettingservicejava"></a>

```java
package com.portfolio.service;

import com.portfolio.dto.ServiceItem;
import com.portfolio.entity.SiteSetting;
import com.portfolio.repository.SiteSettingRepository;
import org.springframework.stereotype.Service;
import org.springframework.transaction.annotation.Transactional;

import java.time.LocalDateTime;
import java.util.ArrayList;
import java.util.HashMap;
import java.util.List;
import java.util.Map;

/**
 * ============================================================================
 * SERVICE : SiteSettingService
 * ============================================================================
 * Reads and writes the key/value rows that drive the profile pages
 * (hero name, career objective, social links, services, ...).
 *
 * Every read is null safe: if a key is missing the default supplied by the
 * caller is returned, so the public site never renders a blank page just
 * because a setting was deleted.
 * ============================================================================
 */
@Service
@Transactional
public class SiteSettingService {

    private final SiteSettingRepository settingRepository;
    private final com.portfolio.repository.AdminUserRepository adminUserRepository;

    public SiteSettingService(SiteSettingRepository settingRepository,
                              com.portfolio.repository.AdminUserRepository adminUserRepository) {
        this.settingRepository = settingRepository;
        this.adminUserRepository = adminUserRepository;
    }

    /** One setting value, or {@code defaultValue} when the key is missing. */
    @Transactional(readOnly = true)
    public String getValue(String key, String defaultValue) {
        return settingRepository.findByUserIsNullAndKey(key)
                .or(() -> settingRepository.findFirstByKey(key))
                .map(SiteSetting::getValue)
                .filter(value -> value != null && !value.isBlank())
                .orElse(defaultValue);
    }

    /** One setting value, or "" when the key is missing. */
    @Transactional(readOnly = true)
    public String getValue(String key) {
        return getValue(key, "");
    }

    /** User-scoped setting value with fallback to global. */
    @Transactional(readOnly = true)
    public String getValue(com.portfolio.entity.AdminUser user, String key, String defaultValue) {
        if (user == null) {
            return getValue(key, defaultValue);
        }
        return settingRepository.findByUserAndKey(user, key)
                .map(SiteSetting::getValue)
                .filter(v -> v != null && !v.isBlank())
                .orElseGet(() -> getValue(key, defaultValue));
    }

    /**
     * The whole settings table as a Map, ready to be dropped into a model.
     * Thymeleaf can then use {@code ${settings['hero.name']}}.
     */
    @Transactional(readOnly = true)
    public Map<String, String> getSettingsMap() {
        Map<String, String> map = new HashMap<>();
        for (SiteSetting setting : settingRepository.findByUserIsNull()) {
            map.put(setting.getKey(), setting.getValue() == null ? "" : setting.getValue());
        }
        return map;
    }

    /**
     * User-scoped settings map with user profile overrides.
     */
    @Transactional(readOnly = true)
    public Map<String, String> getSettingsMap(com.portfolio.entity.AdminUser user) {
        Map<String, String> map = new HashMap<>(getSettingsMap());
        if (user == null) {
            return map;
        }

        // Apply direct User entity profile fields
        if (user.getFullName() != null) map.put("hero.name", user.getFullName());
        if (user.getHeadline() != null) map.put("hero.title", user.getHeadline());
        if (user.getBio() != null) {
            map.put("hero.intro", user.getBio());
            map.put("about.bio", user.getBio());
        }
        if (user.getEmail() != null) map.put("about.email", user.getEmail());
        if (user.getPhone() != null) map.put("about.phone", user.getPhone());
        if (user.getLocation() != null) map.put("about.location", user.getLocation());
        if (user.getAvatarUrl() != null) map.put("profile.image", user.getAvatarUrl());
        if (user.getGithubUrl() != null) map.put("social.github", user.getGithubUrl());
        if (user.getLinkedinUrl() != null) map.put("social.linkedin", user.getLinkedinUrl());
        if (user.getTwitterUrl() != null) map.put("social.twitter", user.getTwitterUrl());

        // Apply any user-specific site_settings overrides
        for (SiteSetting setting : settingRepository.findByUser(user)) {
            map.put(setting.getKey(), setting.getValue() == null ? "" : setting.getValue());
        }
        return map;
    }

    /** Create or update one setting (used by the admin Settings page). */
    public void saveValue(String key, String value, String label) {
        SiteSetting setting = settingRepository.findByUserIsNullAndKey(key)
                .orElseGet(() -> new SiteSetting(key, value, label));
        setting.setValue(value);
        if (label != null && !label.isBlank()) {
            setting.setLabel(label);
        }
        setting.setUpdatedAt(LocalDateTime.now());
        settingRepository.save(setting);
    }

    /** Save setting for a specific user. */
    public void saveValue(com.portfolio.entity.AdminUser user, String key, String value, String label) {
        if (user == null) {
            saveValue(key, value, label);
            return;
        }
        SiteSetting setting = settingRepository.findByUserAndKey(user, key)
                .orElseGet(() -> new SiteSetting(user, key, value, label));
        setting.setValue(value);
        if (label != null && !label.isBlank()) {
            setting.setLabel(label);
        }
        setting.setUpdatedAt(LocalDateTime.now());
        settingRepository.save(setting);

        // Sync changes back to AdminUser entity where applicable
        boolean changed = false;
        if ("hero.name".equals(key) && value != null) { user.setFullName(value); changed = true; }
        else if ("hero.title".equals(key) && value != null) { user.setHeadline(value); changed = true; }
        else if ("hero.intro".equals(key) && value != null) { user.setBio(value); changed = true; }
        else if ("about.email".equals(key) && value != null) { user.setEmail(value); changed = true; }
        else if ("about.phone".equals(key) && value != null) { user.setPhone(value); changed = true; }
        else if ("about.location".equals(key) && value != null) { user.setLocation(value); changed = true; }
        else if ("profile.image".equals(key) && value != null) { user.setAvatarUrl(value); changed = true; }
        else if ("social.github".equals(key) && value != null) { user.setGithubUrl(value); changed = true; }
        else if ("social.linkedin".equals(key) && value != null) { user.setLinkedinUrl(value); changed = true; }
        else if ("social.twitter".equals(key) && value != null) { user.setTwitterUrl(value); changed = true; }

        if (changed) {
            adminUserRepository.save(user);
        }
    }

    /** Stores a key only when it does not exist yet (used by the data seeder). */
    public void saveIfAbsent(String key, String value, String label) {
        if (settingRepository.findByUserIsNullAndKey(key).isEmpty()) {
            settingRepository.save(new SiteSetting(key, value, label));
        }
    }

    /** Stores a key for a specific user only when it does not exist yet. */
    public void saveIfAbsent(com.portfolio.entity.AdminUser user, String key, String value, String label) {
        if (user == null) {
            saveIfAbsent(key, value, label);
            return;
        }
        if (settingRepository.findByUserAndKey(user, key).isEmpty()) {
            settingRepository.save(new SiteSetting(user, key, value, label));
        }
    }

    /**
     * The "What I Do" cards, parsed from the multi-line {@code services.list}
     * setting. One line = one card, in the format icon|title|description.
     */
    @Transactional(readOnly = true)
    public List<ServiceItem> getServices() {
        return getServices((com.portfolio.entity.AdminUser) null);
    }

    @Transactional(readOnly = true)
    public List<ServiceItem> getServices(com.portfolio.entity.AdminUser user) {
        String raw = getValue(user, com.portfolio.entity.SettingKey.SERVICES, "");
        if (raw == null || raw.isBlank()) {
            raw = getValue(com.portfolio.entity.SettingKey.SERVICES, "");
        }
        List<ServiceItem> services = new ArrayList<>();
        for (String line : raw.split("\\r?\\n")) {
            ServiceItem item = ServiceItem.fromLine(line);
            if (item != null) {
                services.add(item);
            }
        }
        return services;
    }

    @Transactional(readOnly = true)
    public List<SiteSetting> getAll(com.portfolio.entity.AdminUser user) {
        if (user == null) {
            return getAll();
        }
        List<SiteSetting> userSettings = settingRepository.findByUser(user);
        if (userSettings.isEmpty()) {
            return getAll();
        }
        return userSettings;
    }

    /** All global setting rows - used by default when no user is specified. */
    @Transactional(readOnly = true)
    public List<SiteSetting> getAll() {
        List<SiteSetting> globalSettings = settingRepository.findByUserIsNull();
        return globalSettings.isEmpty() ? settingRepository.findAll() : globalSettings;
    }
}

```

---

## `portfolio-app/src/main/java/com/portfolio/service/SkillService.java`
<a id="portfolio-app-src-main-java-com-portfolio-service-skillservicejava"></a>

```java
package com.portfolio.service;

import com.portfolio.entity.Skill;

import java.util.LinkedHashMap;
import java.util.List;
import java.util.Map;

/**
 * ============================================================================
 * SERVICE INTERFACE : SkillService
 * ============================================================================
 */
public interface SkillService {

    List<Skill> getAllSkills();

    List<Skill> searchSkills(String keyword);

    /**
     * Skills grouped by category, ready for the public page.
     * A {@code LinkedHashMap} keeps the categories in the order the query
     * returned them, so "Programming Languages" is always above "Tools".
     */
    Map<String, List<Skill>> getSkillsGroupedByCategory();

    List<String> getAllCategories();

    Skill getSkillById(Long id);

    Skill saveSkill(Skill skill);

    void deleteSkill(Long id);

    long countAll();

    // =====================================================================
    //  USER-SCOPED METHODS
    // =====================================================================

    List<Skill> getAllSkills(com.portfolio.entity.AdminUser user);

    List<Skill> searchSkills(com.portfolio.entity.AdminUser user, String keyword);

    Map<String, List<Skill>> getSkillsGroupedByCategory(com.portfolio.entity.AdminUser user);

    List<String> getAllCategories(com.portfolio.entity.AdminUser user);

    Skill getSkillByIdAndUser(Long id, com.portfolio.entity.AdminUser user);

    long countAll(com.portfolio.entity.AdminUser user);
}

```

---

## `portfolio-app/src/main/java/com/portfolio/service/SkillServiceImpl.java`
<a id="portfolio-app-src-main-java-com-portfolio-service-skillserviceimpljava"></a>

```java
package com.portfolio.service;

import com.portfolio.entity.Skill;
import com.portfolio.exception.ResourceNotFoundException;
import com.portfolio.repository.SkillRepository;
import org.springframework.stereotype.Service;
import org.springframework.transaction.annotation.Transactional;

import java.util.LinkedHashMap;
import java.util.List;
import java.util.Map;

/**
 * ============================================================================
 * SERVICE IMPLEMENTATION : SkillServiceImpl
 * ============================================================================
 */
@Service
@Transactional
public class SkillServiceImpl implements SkillService {

    private final SkillRepository skillRepository;

    public SkillServiceImpl(SkillRepository skillRepository) {
        this.skillRepository = skillRepository;
    }

    @Override
    @Transactional(readOnly = true)
    public List<Skill> getAllSkills() {
        return skillRepository.findAllByOrderByCategoryAscSortOrderAscNameAsc();
    }

    @Override
    @Transactional(readOnly = true)
    public List<Skill> searchSkills(String keyword) {
        if (keyword == null || keyword.isBlank()) {
            return getAllSkills();
        }
        return skillRepository.searchByKeyword(keyword.trim());
    }

    /**
     * Groups the flat skill list into { category -> [skills] }.
     *
     * Doing this in Java (instead of running one query per category) means a
     * single round trip to MySQL, which is faster and is the pattern you
     * should describe in a viva when asked "how did you avoid N+1 queries".
     */
    @Override
    @Transactional(readOnly = true)
    public Map<String, List<Skill>> getSkillsGroupedByCategory() {
        Map<String, List<Skill>> grouped = new LinkedHashMap<>();
        for (Skill skill : getAllSkills()) {
            String category = (skill.getCategory() == null || skill.getCategory().isBlank())
                    ? "Other Technologies"
                    : skill.getCategory();
            grouped.computeIfAbsent(category, key -> new java.util.ArrayList<>()).add(skill);
        }
        return grouped;
    }

    @Override
    @Transactional(readOnly = true)
    public List<String> getAllCategories() {
        return skillRepository.findAllCategories();
    }

    @Override
    @Transactional(readOnly = true)
    public Skill getSkillById(Long id) {
        return skillRepository.findById(id)
                .orElseThrow(() -> new ResourceNotFoundException("Skill not found with id: " + id));
    }

    @Override
    public Skill saveSkill(Skill skill) {
        // Guard rails - the form validates too, but the service is the last line
        // of defence before data reaches the database.
        if (skill.getProficiency() == null || skill.getProficiency() < 0) {
            skill.setProficiency(0);
        }
        if (skill.getProficiency() > 100) {
            skill.setProficiency(100);
        }
        return skillRepository.save(skill);
    }

    @Override
    public void deleteSkill(Long id) {
        if (!skillRepository.existsById(id)) {
            throw new ResourceNotFoundException("Skill not found with id: " + id);
        }
        skillRepository.deleteById(id);
    }

    @Override
    @Transactional(readOnly = true)
    public long countAll() {
        return skillRepository.count();
    }

    // =====================================================================
    //  USER-SCOPED IMPLEMENTATIONS
    // =====================================================================

    @Override
    @Transactional(readOnly = true)
    public List<Skill> getAllSkills(com.portfolio.entity.AdminUser user) {
        if (user == null) {
            return getAllSkills();
        }
        return skillRepository.findByUserOrderByCategoryAscSortOrderAscNameAsc(user);
    }

    @Override
    @Transactional(readOnly = true)
    public List<Skill> searchSkills(com.portfolio.entity.AdminUser user, String keyword) {
        if (user == null) {
            return searchSkills(keyword);
        }
        if (keyword == null || keyword.isBlank()) {
            return getAllSkills(user);
        }
        return skillRepository.searchByUserAndKeyword(user, keyword.trim());
    }

    @Override
    @Transactional(readOnly = true)
    public Map<String, List<Skill>> getSkillsGroupedByCategory(com.portfolio.entity.AdminUser user) {
        if (user == null) {
            return getSkillsGroupedByCategory();
        }
        Map<String, List<Skill>> grouped = new LinkedHashMap<>();
        for (Skill skill : getAllSkills(user)) {
            String category = (skill.getCategory() == null || skill.getCategory().isBlank())
                    ? "Other Technologies"
                    : skill.getCategory();
            grouped.computeIfAbsent(category, key -> new java.util.ArrayList<>()).add(skill);
        }
        return grouped;
    }

    @Override
    @Transactional(readOnly = true)
    public List<String> getAllCategories(com.portfolio.entity.AdminUser user) {
        if (user == null) {
            return getAllCategories();
        }
        return skillRepository.findCategoriesByUser(user);
    }

    @Override
    @Transactional(readOnly = true)
    public Skill getSkillByIdAndUser(Long id, com.portfolio.entity.AdminUser user) {
        if (user == null) {
            return getSkillById(id);
        }
        return skillRepository.findByIdAndUser(id, user)
                .orElseThrow(() -> new ResourceNotFoundException("Skill not found with id: " + id));
    }

    @Override
    @Transactional(readOnly = true)
    public long countAll(com.portfolio.entity.AdminUser user) {
        if (user == null) {
            return countAll();
        }
        return skillRepository.countByUser(user);
    }
}

```

---

## `portfolio-app/src/main/java/com/portfolio/service/UserService.java`
<a id="portfolio-app-src-main-java-com-portfolio-service-userservicejava"></a>

```java
package com.portfolio.service;

import com.portfolio.dto.RegisterForm;
import com.portfolio.entity.AdminUser;
import com.portfolio.entity.Education;
import com.portfolio.entity.Experience;
import com.portfolio.entity.Project;
import com.portfolio.entity.ProjectCategory;
import com.portfolio.entity.Skill;
import com.portfolio.repository.AdminUserRepository;
import com.portfolio.repository.EducationRepository;
import com.portfolio.repository.ExperienceRepository;
import com.portfolio.repository.ProjectRepository;
import com.portfolio.repository.SkillRepository;
import org.springframework.security.crypto.password.PasswordEncoder;
import org.springframework.stereotype.Service;
import org.springframework.transaction.annotation.Transactional;

import java.time.LocalDate;
import java.util.List;
import java.util.Optional;

/**
 * ============================================================================
 * SERVICE : UserService
 * ============================================================================
 * Handles user self-registration, starter portfolio population, and querying
 * creators for the Explore directory.
 * ============================================================================
 */
@Service
@Transactional
public class UserService {

    private final AdminUserRepository adminUserRepository;
    private final ProjectRepository projectRepository;
    private final SkillRepository skillRepository;
    private final EducationRepository educationRepository;
    private final ExperienceRepository experienceRepository;
    private final PasswordEncoder passwordEncoder;

    public UserService(AdminUserRepository adminUserRepository,
                       ProjectRepository projectRepository,
                       SkillRepository skillRepository,
                       EducationRepository educationRepository,
                       ExperienceRepository experienceRepository,
                       PasswordEncoder passwordEncoder) {
        this.adminUserRepository = adminUserRepository;
        this.projectRepository = projectRepository;
        this.skillRepository = skillRepository;
        this.educationRepository = educationRepository;
        this.experienceRepository = experienceRepository;
        this.passwordEncoder = passwordEncoder;
    }

    /**
     * Registers a new user and seeds an initial starter portfolio for them.
     */
    public AdminUser registerUser(RegisterForm form) {
        String username = form.getUsername().toLowerCase().trim();
        String email = form.getEmail().toLowerCase().trim();

        if (adminUserRepository.existsByUsername(username)) {
            throw new IllegalArgumentException("Username '" + username + "' is already taken.");
        }
        if (adminUserRepository.existsByEmail(email)) {
            throw new IllegalArgumentException("An account with email '" + email + "' already exists.");
        }

        AdminUser user = new AdminUser(
                username,
                email,
                passwordEncoder.encode(form.getPassword()),
                form.getFullName().trim(),
                "ROLE_ADMIN" // Grants access to their personal portfolio management dashboard
        );

        String headline = (form.getHeadline() != null && !form.getHeadline().isBlank())
                ? form.getHeadline().trim()
                : "Software Developer";
        user.setHeadline(headline);
        user.setBio("Hello! I am " + form.getFullName().trim() + ", a passionate " + headline +
                ". Welcome to my personal portfolio. Feel free to explore my work and reach out!");
        user.setAvatarUrl("/img/profile-placeholder.svg");

        AdminUser savedUser = adminUserRepository.save(user);

        // Seed initial starter portfolio items so the new user's portfolio looks great immediately
        seedStarterPortfolio(savedUser);

        return savedUser;
    }

    private void seedStarterPortfolio(AdminUser user) {
        // 1. Starter Project
        Project project = new Project();
        project.setUser(user);
        project.setTitle("Personal Portfolio Platform");
        project.setDescription("A responsive multi-user portfolio web application built with Spring Boot, Thymeleaf, and JPA.");
        project.setProblemStatement("Software engineers need a modern personal showcase to display their work, manage skills, and receive messages from potential clients or recruiters.");
        project.setFeatures("Custom developer profile\nSkills showcase\nProject highlights\nContact inbox");
        project.setCategory(ProjectCategory.WEB);
        project.setTechnologies("Java, Spring Boot, Thymeleaf, JPA, HTML5/CSS3");
        project.setImageUrl("/img/project-placeholder.svg");
        project.setFeatured(true);
        project.setSortOrder(1);
        projectRepository.save(project);

        // 2. Starter Skills
        Skill s1 = new Skill("Java", "Backend", 85, 1);
        s1.setUser(user);
        skillRepository.save(s1);

        Skill s2 = new Skill("Spring Boot", "Backend", 80, 2);
        s2.setUser(user);
        skillRepository.save(s2);

        Skill s3 = new Skill("HTML & CSS", "Frontend", 85, 3);
        s3.setUser(user);
        skillRepository.save(s3);

        Skill s4 = new Skill("Git & GitHub", "Tools", 90, 4);
        s4.setUser(user);
        skillRepository.save(s4);

        // 3. Starter Education
        Education edu = new Education(
                "Bachelor of Technology / Engineering",
                "University / College Institute",
                LocalDate.now().getYear() - 3,
                LocalDate.now().getYear() + 1,
                "Current Student",
                "Studying Computer Science / Software Engineering with core focus on algorithms, data structures, and web technologies.",
                1
        );
        edu.setUser(user);
        educationRepository.save(edu);

        // 4. Starter Experience
        Experience exp = new Experience(
                user.getHeadline() != null ? user.getHeadline() : "Software Developer",
                "Independent Projects & Freelance",
                LocalDate.now().minusYears(1),
                null,
                "Designing and developing modern web applications.\nCollaborating on open-source repositories and building full-stack solutions.",
                "Java, Spring Boot, MySQL, Git",
                1
        );
        exp.setUser(user);
        experienceRepository.save(exp);
    }

    @Transactional(readOnly = true)
    public Optional<AdminUser> findByUsername(String username) {
        return adminUserRepository.findByUsername(username.toLowerCase().trim());
    }

    @Transactional(readOnly = true)
    public Optional<AdminUser> findByEmail(String email) {
        return adminUserRepository.findByEmail(email.toLowerCase().trim());
    }

    @Transactional(readOnly = true)
    public Optional<AdminUser> findByUsernameOrEmail(String identifier) {
        return adminUserRepository.findByUsernameOrEmail(identifier.trim(), identifier.trim());
    }

    @Transactional(readOnly = true)
    public List<AdminUser> getAllPublicUsers() {
        return adminUserRepository.findByEnabledTrueOrderByCreatedAtDesc();
    }

    @Transactional(readOnly = true)
    public List<AdminUser> searchPublicUsers(String keyword) {
        if (keyword == null || keyword.isBlank()) {
            return getAllPublicUsers();
        }
        String term = keyword.toLowerCase().trim();
        return adminUserRepository.findByEnabledTrueOrderByCreatedAtDesc().stream()
                .filter(u -> (u.getFullName() != null && u.getFullName().toLowerCase().contains(term))
                        || (u.getUsername() != null && u.getUsername().toLowerCase().contains(term))
                        || (u.getHeadline() != null && u.getHeadline().toLowerCase().contains(term))
                        || (u.getBio() != null && u.getBio().toLowerCase().contains(term)))
                .toList();
    }
}

```

---

# 7. Security & Authentication Services

## `portfolio-app/src/main/java/com/portfolio/security/AuthHelper.java`
<a id="portfolio-app-src-main-java-com-portfolio-security-authhelperjava"></a>

```java
package com.portfolio.security;

import com.portfolio.entity.AdminUser;
import com.portfolio.repository.AdminUserRepository;
import org.springframework.security.authentication.AnonymousAuthenticationToken;
import org.springframework.security.core.Authentication;
import org.springframework.security.core.context.SecurityContextHolder;
import org.springframework.stereotype.Component;

import java.util.Optional;

/**
 * ============================================================================
 * HELPER : AuthHelper
 * ============================================================================
 * Provides convenient methods to extract the currently authenticated AdminUser
 * from Spring Security's SecurityContextHolder.
 * ============================================================================
 */
@Component
public class AuthHelper {

    private final AdminUserRepository adminUserRepository;

    public AuthHelper(AdminUserRepository adminUserRepository) {
        this.adminUserRepository = adminUserRepository;
    }

    /**
     * Returns true if a user is currently logged in (not anonymous).
     */
    public boolean isAuthenticated() {
        Authentication auth = SecurityContextHolder.getContext().getAuthentication();
        return auth != null && auth.isAuthenticated() && !(auth instanceof AnonymousAuthenticationToken);
    }

    /**
     * Returns an Optional containing the logged-in AdminUser, or empty if anonymous.
     */
    public Optional<AdminUser> getCurrentUserOptional() {
        if (!isAuthenticated()) {
            return Optional.empty();
        }
        Authentication auth = SecurityContextHolder.getContext().getAuthentication();
        String identifier = auth.getName();
        return adminUserRepository.findByUsernameOrEmail(identifier, identifier);
    }

    /**
     * Returns the currently logged in AdminUser. Throws an IllegalStateException
     * if called when no user is authenticated.
     */
    public AdminUser getCurrentUser() {
        return getCurrentUserOptional().orElseThrow(() ->
                new IllegalStateException("No authenticated user found in security context"));
    }
}

```

---

## `portfolio-app/src/main/java/com/portfolio/security/CustomUserDetailsService.java`
<a id="portfolio-app-src-main-java-com-portfolio-security-customuserdetailsservicejava"></a>

```java
package com.portfolio.security;

import com.portfolio.entity.AdminUser;
import com.portfolio.repository.AdminUserRepository;
import org.springframework.security.core.userdetails.User;
import org.springframework.security.core.userdetails.UserDetails;
import org.springframework.security.core.userdetails.UserDetailsService;
import org.springframework.security.core.userdetails.UsernameNotFoundException;
import org.springframework.stereotype.Service;
import org.springframework.transaction.annotation.Transactional;

/**
 * ============================================================================
 * SECURITY : CustomUserDetailsService
 * ============================================================================
 * Spring Security calls {@code loadUserByUsername()} during login. This class
 * is the bridge between Spring Security and OUR database:
 *
 *   1. Spring Security receives username + password from the login form
 *   2. it calls loadUserByUsername(username)
 *   3. we read the admin_users row and return a Spring Security UserDetails
 *   4. Spring Security compares the submitted password against the stored
 *      BCrypt hash using the PasswordEncoder bean
 *
 * If the username is unknown we throw UsernameNotFoundException and the user
 * is sent back to /admin/login?error.
 * ============================================================================
 */
@Service
public class CustomUserDetailsService implements UserDetailsService {

    private final AdminUserRepository adminUserRepository;

    public CustomUserDetailsService(AdminUserRepository adminUserRepository) {
        this.adminUserRepository = adminUserRepository;
    }

    @Override
    @Transactional(readOnly = true)
    public UserDetails loadUserByUsername(String identifier) throws UsernameNotFoundException {
        AdminUser adminUser = adminUserRepository.findByUsernameOrEmail(identifier.trim(), identifier.trim())
                .orElseThrow(() -> new UsernameNotFoundException(
                        "No account found with username or email: " + identifier));

        // User.withUsername(...) builds the object Spring Security expects.
        // authorities(adminUser.getRole()) -> "ROLE_ADMIN"
        // .disabled(!enabled)               -> a disabled account cannot log in
        return User.withUsername(adminUser.getUsername())
                .password(adminUser.getPassword())
                .authorities(adminUser.getRole())
                .disabled(!adminUser.isEnabled())
                .accountExpired(false)
                .accountLocked(false)
                .credentialsExpired(false)
                .build();
    }
}

```

---

# 8. Database Initialization & Exception Handling

## `portfolio-app/src/main/java/com/portfolio/init/DataSeeder.java`
<a id="portfolio-app-src-main-java-com-portfolio-init-dataseederjava"></a>

```java
package com.portfolio.init;

import com.portfolio.config.PortfolioProfileData;
import com.portfolio.entity.AdminUser;
import com.portfolio.entity.Education;
import com.portfolio.entity.Project;
import com.portfolio.entity.ProjectCategory;
import com.portfolio.entity.SettingKey;
import com.portfolio.entity.Skill;
import com.portfolio.repository.AchievementRepository;
import com.portfolio.repository.AdminUserRepository;
import com.portfolio.repository.CertificationRepository;
import com.portfolio.repository.EducationRepository;
import com.portfolio.repository.ExperienceRepository;
import com.portfolio.repository.ProjectRepository;
import com.portfolio.repository.SkillRepository;
import com.portfolio.service.SiteSettingService;
import org.slf4j.Logger;
import org.slf4j.LoggerFactory;
import org.springframework.beans.factory.annotation.Value;
import org.springframework.boot.CommandLineRunner;
import org.springframework.security.crypto.password.PasswordEncoder;
import org.springframework.stereotype.Component;
import org.springframework.transaction.annotation.Transactional;

import java.util.List;

/**
 * ============================================================================
 * DATA SEEDER  (runs on application startup)
 * ============================================================================
 * Populates real profile data for Vaishnavi Sunil Mali based on the centralized
 * definitions in {@link PortfolioProfileData}.
 *
 * Ensures:
 *   1. Real owner account and profile settings exist.
 *   2. Clean, accurate sample projects (IoT, Student Management, Portfolio).
 *   3. Real technical skills spanning EXTC, Programming, Web, Databases, and Tools.
 *   4. Zero fabrication: No fake internships, employers, certificates, or awards.
 *   5. Legacy placeholder / dummy user cleanup.
 * ============================================================================
 */
@Component
public class DataSeeder implements CommandLineRunner {

    private static final Logger log = LoggerFactory.getLogger(DataSeeder.class);

    private final AdminUserRepository adminUserRepository;
    private final ProjectRepository projectRepository;
    private final SkillRepository skillRepository;
    private final EducationRepository educationRepository;
    private final ExperienceRepository experienceRepository;
    private final CertificationRepository certificationRepository;
    private final AchievementRepository achievementRepository;
    private final SiteSettingService siteSettingService;
    private final PasswordEncoder passwordEncoder;

    @Value("${app.security.default-admin-username:vaishnavi}")
    private String defaultAdminUsername;

    @Value("${app.security.default-admin-password:ChangeMe@123}")
    private String defaultAdminPassword;

    @Value("${app.seed.enabled:true}")
    private boolean seedEnabled;

    public DataSeeder(AdminUserRepository adminUserRepository,
                      ProjectRepository projectRepository,
                      SkillRepository skillRepository,
                      EducationRepository educationRepository,
                      ExperienceRepository experienceRepository,
                      CertificationRepository certificationRepository,
                      AchievementRepository achievementRepository,
                      SiteSettingService siteSettingService,
                      PasswordEncoder passwordEncoder) {
        this.adminUserRepository = adminUserRepository;
        this.projectRepository = projectRepository;
        this.skillRepository = skillRepository;
        this.educationRepository = educationRepository;
        this.experienceRepository = experienceRepository;
        this.certificationRepository = certificationRepository;
        this.achievementRepository = achievementRepository;
        this.siteSettingService = siteSettingService;
        this.passwordEncoder = passwordEncoder;
    }

    @Override
    @Transactional
    public void run(String... args) {
        cleanupLegacyDemoData();
        AdminUser admin = seedAdminUser();
        if (seedEnabled) {
            seedPortfolioData(admin);
        }
    }

    /** Cleans up legacy placeholder demo users and fake entries if previously seeded. */
    private void cleanupLegacyDemoData() {
        // Clean up legacy "janedoe"
        adminUserRepository.findByUsername("janedoe").ifPresent(jane -> {
            projectRepository.findAll().stream()
                    .filter(p -> p.getUser() != null && jane.getId().equals(p.getUser().getId()))
                    .forEach(projectRepository::delete);
            skillRepository.findAll().stream()
                    .filter(s -> s.getUser() != null && jane.getId().equals(s.getUser().getId()))
                    .forEach(skillRepository::delete);
            educationRepository.findAll().stream()
                    .filter(e -> e.getUser() != null && jane.getId().equals(e.getUser().getId()))
                    .forEach(educationRepository::delete);
            experienceRepository.findAll().stream()
                    .filter(exp -> exp.getUser() != null && jane.getId().equals(exp.getUser().getId()))
                    .forEach(experienceRepository::delete);
            certificationRepository.findAll().stream()
                    .filter(c -> c.getUser() != null && jane.getId().equals(c.getUser().getId()))
                    .forEach(certificationRepository::delete);
            achievementRepository.findAll().stream()
                    .filter(a -> a.getUser() != null && jane.getId().equals(a.getUser().getId()))
                    .forEach(achievementRepository::delete);
            adminUserRepository.delete(jane);
            log.info("Cleaned up legacy demo user 'janedoe'.");
        });

        // Clean up fake experience if it contains placeholder companies
        experienceRepository.findAll().stream()
                .filter(exp -> exp.getOrganization() != null && exp.getOrganization().contains("Your Company Name"))
                .forEach(experienceRepository::delete);

        // Clean up fake certifications with placeholder links or issuers
        certificationRepository.findAll().stream()
                .filter(cert -> (cert.getCertificateUrl() != null && cert.getCertificateUrl().contains("your-certificate-link"))
                        || (cert.getIssuer() != null && cert.getIssuer().contains("Your Certification Provider")))
                .forEach(certificationRepository::delete);

        // Clean up fake achievements
        achievementRepository.findAll().stream()
                .filter(ach -> ach.getOrganization() != null && ach.getOrganization().contains("Your Organising Institute"))
                .forEach(achievementRepository::delete);
    }

    /**
     * Seeds or updates the primary admin user with Vaishnavi Sunil Mali's credentials.
     */
    private AdminUser seedAdminUser() {
        AdminUser admin = adminUserRepository.findByUsername(defaultAdminUsername)
                .or(() -> adminUserRepository.findByEmail(PortfolioProfileData.EMAIL))
                .or(() -> adminUserRepository.findByUsername("admin"))
                .orElse(null);

        if (admin == null) {
            admin = new AdminUser(
                    defaultAdminUsername,
                    passwordEncoder.encode(defaultAdminPassword),
                    PortfolioProfileData.FULL_NAME,
                    "ROLE_ADMIN"
            );
            admin.setEmail(PortfolioProfileData.EMAIL);
            admin.setHeadline(PortfolioProfileData.HEADLINE);
            admin.setBio(PortfolioProfileData.ABOUT_INTRO);
            admin.setLocation(PortfolioProfileData.LOCATION);
            admin = adminUserRepository.save(admin);
            log.info("Created primary portfolio admin user: {} ({})", admin.getUsername(), admin.getEmail());
        } else {
            // Update to real details if old placeholders remain
            boolean updated = false;
            if ("Admin User".equals(admin.getFullName()) || "Your Name".equals(admin.getFullName())) {
                admin.setFullName(PortfolioProfileData.FULL_NAME);
                updated = true;
            }
            if ("admin@portfolio.local".equals(admin.getEmail()) || "your.email@example.com".equals(admin.getEmail())) {
                admin.setEmail(PortfolioProfileData.EMAIL);
                updated = true;
            }
            if (admin.getHeadline() == null || admin.getHeadline().contains("Lead Architect") || admin.getHeadline().contains("Computer Engineering")) {
                admin.setHeadline(PortfolioProfileData.HEADLINE);
                updated = true;
            }
            if (admin.getLocation() == null || admin.getLocation().contains("Your City")) {
                admin.setLocation(PortfolioProfileData.LOCATION);
                updated = true;
            }
            if (updated) {
                admin = adminUserRepository.save(admin);
                log.info("Updated admin user profile to {}", admin.getFullName());
            }
        }
        return admin;
    }

    private void seedPortfolioData(AdminUser admin) {
        seedSettings(admin);
        seedProjects(admin);
        seedSkills(admin);
        seedEducation(admin);
        log.info("Portfolio profile data verified and active for: {}", PortfolioProfileData.FULL_NAME);
    }

    private void seedSettings(AdminUser admin) {
        saveOrUpdateSetting(null, SettingKey.HERO_NAME, PortfolioProfileData.FULL_NAME, "Full Name");
        saveOrUpdateSetting(null, SettingKey.HERO_TITLE, PortfolioProfileData.HEADLINE, "Professional Title");
        saveOrUpdateSetting(null, SettingKey.HERO_INTRO, PortfolioProfileData.SHORT_INTRO, "Short Introduction");
        saveOrUpdateSetting(null, SettingKey.HERO_TYPING_WORDS, PortfolioProfileData.TYPING_WORDS, "Typing Animation Words");
        saveOrUpdateSetting(null, SettingKey.PROFILE_IMAGE, PortfolioProfileData.PROFILE_IMAGE_URL, "Profile Photo Path");
        saveOrUpdateSetting(null, SettingKey.RESUME_URL, PortfolioProfileData.RESUME_URL, "Resume Download URL");

        saveOrUpdateSetting(null, SettingKey.ABOUT_INTRO, PortfolioProfileData.ABOUT_INTRO, "About Me Paragraph");
        saveOrUpdateSetting(null, SettingKey.ABOUT_OBJECTIVE, PortfolioProfileData.CAREER_OBJECTIVE, "Career Objective");
        saveOrUpdateSetting(null, SettingKey.ABOUT_INTERESTS, PortfolioProfileData.TECHNICAL_INTERESTS, "Interests");
        saveOrUpdateSetting(null, SettingKey.ABOUT_DOB, "", "Date of Birth");
        saveOrUpdateSetting(null, SettingKey.ABOUT_EMAIL, PortfolioProfileData.EMAIL, "Email");
        saveOrUpdateSetting(null, SettingKey.ABOUT_PHONE, PortfolioProfileData.PHONE, "Phone");
        saveOrUpdateSetting(null, SettingKey.ABOUT_LOCATION, PortfolioProfileData.LOCATION, "Location");
        saveOrUpdateSetting(null, SettingKey.ABOUT_LANGUAGES, PortfolioProfileData.LANGUAGES, "Languages");

        saveOrUpdateSetting(null, SettingKey.SOCIAL_GITHUB, PortfolioProfileData.GITHUB_URL, "GitHub URL");
        saveOrUpdateSetting(null, SettingKey.SOCIAL_LINKEDIN, PortfolioProfileData.LINKEDIN_URL, "LinkedIn URL");
        saveOrUpdateSetting(null, SettingKey.SOCIAL_TWITTER, PortfolioProfileData.TWITTER_URL, "Twitter / X URL");
        saveOrUpdateSetting(null, SettingKey.SOCIAL_INSTAGRAM, PortfolioProfileData.INSTAGRAM_URL, "Instagram URL");

        saveOrUpdateSetting(null, SettingKey.SERVICES, PortfolioProfileData.SERVICES, "Services (one per line: icon|title|description)");

        if (admin != null) {
            saveOrUpdateSetting(admin, SettingKey.HERO_NAME, PortfolioProfileData.FULL_NAME, "Full Name");
            saveOrUpdateSetting(admin, SettingKey.HERO_TITLE, PortfolioProfileData.HEADLINE, "Professional Title");
            saveOrUpdateSetting(admin, SettingKey.HERO_INTRO, PortfolioProfileData.SHORT_INTRO, "Short Introduction");
            saveOrUpdateSetting(admin, SettingKey.HERO_TYPING_WORDS, PortfolioProfileData.TYPING_WORDS, "Typing Animation Words");
            saveOrUpdateSetting(admin, SettingKey.ABOUT_INTRO, PortfolioProfileData.ABOUT_INTRO, "About Me Paragraph");
            saveOrUpdateSetting(admin, SettingKey.ABOUT_EMAIL, PortfolioProfileData.EMAIL, "Email");
            saveOrUpdateSetting(admin, SettingKey.ABOUT_LOCATION, PortfolioProfileData.LOCATION, "Location");
            saveOrUpdateSetting(admin, SettingKey.SERVICES, PortfolioProfileData.SERVICES, "Services");
        }
    }

    private void saveOrUpdateSetting(AdminUser user, String key, String value, String label) {
        String current = user == null ? siteSettingService.getValue(key) : siteSettingService.getValue(user, key, null);
        if (current == null || current.isBlank() || isPlaceholderValue(current)) {
            siteSettingService.saveValue(user, key, value, label);
        }
    }

    private boolean isPlaceholderValue(String val) {
        return "Your Name".equals(val)
                || val.contains("your.email@example.com")
                || val.contains("Your City")
                || val.contains("Computer Engineering Student")
                || val.contains("https://github.com/your-username")
                || val.contains("https://linkedin.com/in/your-username");
    }

    private void seedProjects(AdminUser admin) {
        // If projects table contains old placeholder projects, clean them up
        boolean hasOldPlaceholders = projectRepository.findAll().stream()
                .anyMatch(p -> "Library Management System".equals(p.getTitle())
                        || "Weather Forecast Web App".equals(p.getTitle())
                        || (p.getGithubUrl() != null && p.getGithubUrl().contains("your-username")));

        if (hasOldPlaceholders) {
            projectRepository.deleteAll();
            log.info("Replaced legacy placeholder projects with real sample projects.");
        }

        if (projectRepository.count() == 0) {
            List<Project> projects = PortfolioProfileData.createDefaultProjects();
            if (admin != null) {
                projects.forEach(p -> p.setUser(admin));
            }
            projectRepository.saveAll(projects);
            log.info("Seeded {} real sample projects for {}", projects.size(), PortfolioProfileData.FULL_NAME);
        }
    }

    private void seedSkills(AdminUser admin) {
        boolean hasOldSkills = skillRepository.findAll().stream()
                .anyMatch(s -> "Data Structures".equals(s.getName()) || "OOP Concepts".equals(s.getName()));

        if (hasOldSkills) {
            skillRepository.deleteAll();
            log.info("Replaced legacy placeholder skills with real technical skills.");
        }

        if (skillRepository.count() == 0) {
            List<Skill> skills = PortfolioProfileData.createDefaultSkills();
            if (admin != null) {
                skills.forEach(s -> s.setUser(admin));
            }
            skillRepository.saveAll(skills);
            log.info("Seeded {} skills across EXTC, Programming, Web, Databases, and Tools.", skills.size());
        }
    }

    private void seedEducation(AdminUser admin) {
        boolean hasOldEducation = educationRepository.findAll().stream()
                .anyMatch(e -> e.getInstitution() != null && e.getInstitution().contains("Your College"));

        if (hasOldEducation) {
            educationRepository.deleteAll();
        }

        if (educationRepository.count() == 0) {
            Education edu = new Education(
                    PortfolioProfileData.EDU_DEGREE,
                    PortfolioProfileData.EDU_INSTITUTION,
                    PortfolioProfileData.EDU_START_YEAR,
                    PortfolioProfileData.EDU_END_YEAR,
                    PortfolioProfileData.EDU_CGPA,
                    PortfolioProfileData.EDU_DESCRIPTION,
                    1
            );
            if (admin != null) {
                edu.setUser(admin);
            }
            educationRepository.save(edu);
            log.info("Seeded education: {} at {}", edu.getDegree(), edu.getInstitution());
        }
    }
}

```

---

## `portfolio-app/src/main/java/com/portfolio/exception/GlobalExceptionHandler.java`
<a id="portfolio-app-src-main-java-com-portfolio-exception-globalexceptionhandlerjava"></a>

```java
package com.portfolio.exception;

import jakarta.servlet.http.HttpServletRequest;
import org.slf4j.Logger;
import org.slf4j.LoggerFactory;
import org.springframework.http.HttpStatus;
import org.springframework.ui.Model;
import org.springframework.web.bind.annotation.ControllerAdvice;
import org.springframework.web.bind.annotation.ExceptionHandler;
import org.springframework.web.bind.annotation.ResponseStatus;
import org.springframework.web.servlet.NoHandlerFoundException;

import java.time.LocalDateTime;

/**
 * ============================================================================
 * GLOBAL EXCEPTION HANDLER
 * ============================================================================
 * {@code @ControllerAdvice} makes this class a catch-all for exceptions thrown
 * by ANY controller in the application. Instead of writing the same try/catch
 * in 30 controller methods, the handling lives here once.
 *
 * Three friendly pages are produced:
 *   ResourceNotFoundException -> error/404   (record does not exist)
 *   IllegalArgumentException  -> error/400   (bad form input, bad file type)
 *   everything else           -> error/500   (unexpected problem)
 *
 * The real cause is written to the server log with Logger.error(...) so it can
 * be debugged, but the visitor only ever sees a clean page.
 * ============================================================================
 */
@ControllerAdvice
public class GlobalExceptionHandler {

    private static final Logger log = LoggerFactory.getLogger(GlobalExceptionHandler.class);

    /** 404 - the requested id is not in the database. */
    @ExceptionHandler(ResourceNotFoundException.class)
    @ResponseStatus(HttpStatus.NOT_FOUND)
    public String handleNotFound(ResourceNotFoundException ex, Model model, HttpServletRequest request) {
        log.warn("Resource not found: {} (requested: {})", ex.getMessage(), request.getRequestURI());
        return errorModel(model, 404, "Page Not Found",
                "The page or record you are looking for does not exist or has been removed.",
                request.getRequestURI());
    }

    /** 400 - the user submitted something invalid (file type, date range...). */
    @ExceptionHandler(IllegalArgumentException.class)
    @ResponseStatus(HttpStatus.BAD_REQUEST)
    public String handleBadRequest(IllegalArgumentException ex, Model model, HttpServletRequest request) {
        log.warn("Bad request: {} (requested: {})", ex.getMessage(), request.getRequestURI());
        return errorModel(model, 400, "Invalid Request", ex.getMessage(), request.getRequestURI());
    }

    /** 404 - no controller method matches the URL. */
    @ExceptionHandler(NoHandlerFoundException.class)
    @ResponseStatus(HttpStatus.NOT_FOUND)
    public String handleNoHandler(NoHandlerFoundException ex, Model model, HttpServletRequest request) {
        return errorModel(model, 404, "Page Not Found",
                "The page you are looking for does not exist.", request.getRequestURI());
    }

    /**
     * 404 - the URL matched no controller AND no static file.
     *
     * Since Spring Framework 6.1 the DispatcherServlet raises
     * {@code NoResourceFoundException} (not {@code NoHandlerFoundException})
     * when a path such as /this-does-not-exist reaches the resource handler
     * and nothing is there. Without this method it would fall through to the
     * generic handler below and the visitor would see a 500.
     */
    @ExceptionHandler(org.springframework.web.servlet.resource.NoResourceFoundException.class)
    @ResponseStatus(HttpStatus.NOT_FOUND)
    public String handleNoResource(
            org.springframework.web.servlet.resource.NoResourceFoundException ex,
            Model model,
            HttpServletRequest request) {
        log.warn("No handler or static resource for {}", request.getRequestURI());
        return errorModel(model, 404, "Page Not Found",
                "The page you are looking for does not exist.", request.getRequestURI());
    }

    /** 500 - anything unexpected. Details stay in the log, not on the page. */
    @ExceptionHandler(Exception.class)
    @ResponseStatus(HttpStatus.INTERNAL_SERVER_ERROR)
    public String handleGeneric(Exception ex, Model model, HttpServletRequest request) {
        log.error("Unhandled exception on {}: {}", request.getRequestURI(), ex.getMessage(), ex);
        return errorModel(model, 500, "Something Went Wrong",
                "An unexpected error occurred. Please try again in a moment.",
                request.getRequestURI());
    }

    /**
     * IMPORTANT - WHY THESE VALUES ARE SET HERE AND NOT IN A @ModelAttribute
     * ---------------------------------------------------------------------
     * The error templates reuse the shared head / navbar / footer fragments,
     * and those fragments read ${settings['hero.name']}, ${unreadMessages}
     * and ${currentYear}.
     *
     * Attributes contributed by GlobalModelAttributes (@ControllerAdvice +
     * @ModelAttribute) are applied when a HANDLER METHOD is invoked - but they
     * are NOT applied while an exception is being resolved. Relying on a
     * @ModelAttribute here would therefore leave "settings" null and the
     * error page would fail to render, turning a clean 404 into a 500.
     *
     * So every attribute the error templates need is added explicitly below,
     * and the values are hard-coded on purpose: an error page must never
     * depend on the database being reachable.
     */
    private String errorModel(Model model, int status, String title, String message, String path) {
        model.addAttribute("status", status);
        model.addAttribute("title", title);
        model.addAttribute("message", message);
        model.addAttribute("path", path);
        model.addAttribute("timestamp", LocalDateTime.now());

        // Attributes the shared fragments expect (see the note above).
        model.addAttribute("settings", java.util.Map.of(
                "hero.name", "Portfolio",
                "hero.title", "Personal Portfolio"
        ));
        model.addAttribute("services", java.util.List.of());
        model.addAttribute("unreadMessages", 0L);
        model.addAttribute("currentYear", java.time.Year.now().getValue());
        model.addAttribute("activeSection", "");

        return "error/error";
    }
}

```

---

## `portfolio-app/src/main/java/com/portfolio/exception/ResourceNotFoundException.java`
<a id="portfolio-app-src-main-java-com-portfolio-exception-resourcenotfoundexceptionjava"></a>

```java
package com.portfolio.exception;

/**
 * ============================================================================
 * EXCEPTION : ResourceNotFoundException
 * ============================================================================
 * A custom "unchecked" exception (extends RuntimeException, so no forced
 * try/catch everywhere).
 *
 * It is thrown when the service cannot find a row by id, and is translated
 * into the friendly 404 page by {@link GlobalExceptionHandler}. The user sees
 * "Page not found" - never a stack trace.
 * ============================================================================
 */
public class ResourceNotFoundException extends RuntimeException {

    public ResourceNotFoundException(String message) {
        super(message);
    }
}

```

---

# 9. Public & Auth Web Controllers

## `portfolio-app/src/main/java/com/portfolio/controller/PublicController.java`
<a id="portfolio-app-src-main-java-com-portfolio-controller-publiccontrollerjava"></a>

```java
package com.portfolio.controller;

import com.portfolio.dto.DashboardStats;
import com.portfolio.entity.Achievement;
import com.portfolio.entity.Certification;
import com.portfolio.entity.ContactMessage;
import com.portfolio.entity.Education;
import com.portfolio.entity.Experience;
import com.portfolio.entity.Project;
import com.portfolio.entity.ProjectCategory;
import com.portfolio.entity.SettingKey;
import com.portfolio.entity.Skill;
import com.portfolio.service.AchievementService;
import com.portfolio.service.CertificationService;
import com.portfolio.service.ContactMessageService;
import com.portfolio.service.DashboardService;
import com.portfolio.service.EducationService;
import com.portfolio.service.ExperienceService;
import com.portfolio.service.ProjectService;
import com.portfolio.service.SiteSettingService;
import com.portfolio.service.SkillService;
import jakarta.validation.Valid;
import org.springframework.http.ResponseEntity;
import org.springframework.stereotype.Controller;
import org.springframework.ui.Model;
import org.springframework.validation.BindingResult;
import org.springframework.web.bind.annotation.GetMapping;
import org.springframework.web.bind.annotation.ModelAttribute;
import org.springframework.web.bind.annotation.PathVariable;
import org.springframework.web.bind.annotation.PostMapping;
import org.springframework.web.bind.annotation.RequestParam;
import org.springframework.web.servlet.mvc.support.RedirectAttributes;

import java.util.HashMap;
import java.util.List;
import java.util.Map;

/**
 * ============================================================================
 * CONTROLLER : PublicController  (the visitor facing website)
 * ============================================================================
 * One controller for the whole public site. Every method returns the NAME of a
 * Thymeleaf template (a String), and Spring MVC turns that name into a rendered
 * HTML page - that is the "View" part of MVC.
 *
 * FLOW OF A REQUEST
 *   browser  ->  @GetMapping("/projects")  ->  ProjectService  ->  MySQL
 *           <-  model + "public/projects" template  <-  rendered HTML
 *
 * All data comes from the database, so anything changed in the admin panel
 * appears here immediately after a refresh.
 * ============================================================================
 */
@Controller
public class PublicController {

    private final ProjectService projectService;
    private final SkillService skillService;
    private final EducationService educationService;
    private final ExperienceService experienceService;
    private final CertificationService certificationService;
    private final AchievementService achievementService;
    private final ContactMessageService contactMessageService;
    private final DashboardService dashboardService;
    private final SiteSettingService siteSettingService;

    /** Constructor injection - Spring passes all nine services in. */
    public PublicController(ProjectService projectService,
                            SkillService skillService,
                            EducationService educationService,
                            ExperienceService experienceService,
                            CertificationService certificationService,
                            AchievementService achievementService,
                            ContactMessageService contactMessageService,
                            DashboardService dashboardService,
                            SiteSettingService siteSettingService) {
        this.projectService = projectService;
        this.skillService = skillService;
        this.educationService = educationService;
        this.experienceService = experienceService;
        this.certificationService = certificationService;
        this.achievementService = achievementService;
        this.contactMessageService = contactMessageService;
        this.dashboardService = dashboardService;
        this.siteSettingService = siteSettingService;
    }

    // =====================================================================
    //  HOME
    // =====================================================================

    /**
     * GET /
     * The landing page: hero section, a preview of the latest projects, the
     * skill highlights, services and the contact form.
     */
    @GetMapping({"/", "/home"})
    public String home(Model model) {
        // The typing animation needs a list of words, not one string.
        String words = siteSettingService.getValue(SettingKey.HERO_TYPING_WORDS,
                "Java Developer,Spring Boot Developer,Web Developer");
        model.addAttribute("typingWords", splitWords(words));

        // Split the professional title on "|" so the template can style the parts.
        model.addAttribute("titleParts",
                splitWords(siteSettingService.getValue(SettingKey.HERO_TITLE)));

        model.addAttribute("projects", take(projectService.getPublicProjects(), 3));
        model.addAttribute("skills", take(skillService.getAllSkills(), 8));
        model.addAttribute("certifications", take(certificationService.getAll(), 3));
        model.addAttribute("achievements", take(achievementService.getAll(), 4));
        model.addAttribute("stats", buildPublicStats());
        model.addAttribute("contactMessage", new ContactMessage());
        model.addAttribute("activeSection", "home");
        return "public/index";
    }

    // =====================================================================
    //  ABOUT
    // =====================================================================

    /** GET /about */
    @GetMapping("/about")
    public String about(Model model) {
        model.addAttribute("skills", skillService.getAllSkills());
        model.addAttribute("stats", buildPublicStats());
        model.addAttribute("interests",
                splitWords(siteSettingService.getValue(SettingKey.ABOUT_INTERESTS)));
        model.addAttribute("languages",
                splitWords(siteSettingService.getValue(SettingKey.ABOUT_LANGUAGES)));
        model.addAttribute("activeSection", "about");
        return "public/about";
    }

    // =====================================================================
    //  SKILLS
    // =====================================================================

    /** GET /skills - skills grouped by category with progress bars. */
    @GetMapping("/skills")
    public String skills(Model model) {
        model.addAttribute("groupedSkills", skillService.getSkillsGroupedByCategory());
        model.addAttribute("totalSkills", skillService.countAll());
        model.addAttribute("activeSection", "skills");
        return "public/skills";
    }

    // =====================================================================
    //  PROJECTS
    // =====================================================================

    /**
     * GET /projects
     * The grid plus the filter buttons. The optional {@code category} request
     * parameter drives server side filtering, and the JavaScript filter also
     * works client side without a page reload.
     */
    @GetMapping("/projects")
    public String projects(@RequestParam(value = "category", required = false) ProjectCategory category,
                           Model model) {
        model.addAttribute("projects", projectService.getPublicProjectsByCategory(category));
        model.addAttribute("categories", projectService.getAvailableCategories());
        model.addAttribute("selectedCategory", category);
        model.addAttribute("totalProjects", projectService.countPublic());
        model.addAttribute("activeSection", "projects");
        return "public/projects";
    }

    /** GET /projects/{id} - the dedicated project details page. */
    @GetMapping("/projects/{id}")
    public String projectDetails(@PathVariable Long id, Model model) {
        Project project = projectService.getProjectById(id);   // throws -> 404 page
        model.addAttribute("project", project);

        // "More projects" strip at the bottom of the details page.
        List<Project> related = projectService.getPublicProjects().stream()
                .filter(p -> !p.getId().equals(id))
                .limit(3)
                .toList();
        model.addAttribute("relatedProjects", related);
        model.addAttribute("activeSection", "projects");
        return "public/project-details";
    }

    // =====================================================================
    //  EDUCATION / EXPERIENCE
    // =====================================================================

    /** GET /education - vertical timeline. */
    @GetMapping("/education")
    public String education(Model model) {
        model.addAttribute("educations", educationService.getAll());
        model.addAttribute("activeSection", "education");
        return "public/education";
    }

    /** GET /experience - professional timeline. */
    @GetMapping("/experience")
    public String experience(Model model) {
        model.addAttribute("experiences", experienceService.getAll());
        model.addAttribute("activeSection", "experience");
        return "public/experience";
    }

    // =====================================================================
    //  CERTIFICATIONS / ACHIEVEMENTS / SERVICES
    // =====================================================================

    /** GET /certifications */
    @GetMapping("/certifications")
    public String certifications(Model model) {
        model.addAttribute("certifications", certificationService.getAll());
        model.addAttribute("activeSection", "certifications");
        return "public/certifications";
    }

    /** GET /achievements */
    @GetMapping("/achievements")
    public String achievements(Model model) {
        model.addAttribute("achievements", achievementService.getAll());
        model.addAttribute("activeSection", "achievements");
        return "public/achievements";
    }

    /** GET /services - the "What I Do" page. */
    @GetMapping("/services")
    public String servicesPage(Model model) {
        model.addAttribute("activeSection", "services");
        return "public/services";
    }

    // =====================================================================
    //  CONTACT
    // =====================================================================

    /** GET /contact - the page with the form. */
    @GetMapping("/contact")
    public String contact(Model model) {
        if (!model.containsAttribute("contactMessage")) {
            model.addAttribute("contactMessage", new ContactMessage());
        }
        model.addAttribute("activeSection", "contact");
        return "public/contact";
    }

    /**
     * POST /contact/submit  (traditional, no JavaScript needed)
     *
     * {@code @Valid} triggers the annotations on ContactMessage
     * (@NotBlank, @Email, @Size). If anything fails, BindingResult holds the
     * errors and we redisplay the form with the messages instead of saving.
     *
     * RedirectAttributes carries the success message across the redirect, so a
     * browser refresh cannot resubmit the form (the Post/Redirect/Get pattern).
     */
    @PostMapping("/contact/submit")
    public String submitContact(@Valid @ModelAttribute("contactMessage") ContactMessage message,
                                BindingResult bindingResult,
                                RedirectAttributes redirectAttributes,
                                Model model) {
        if (bindingResult.hasErrors()) {
            model.addAttribute("activeSection", "contact");
            return "public/contact";          // back to the form with errors
        }
        contactMessageService.saveMessage(message);
        redirectAttributes.addFlashAttribute("successMessage",
                "Thank you! Your message has been sent successfully.");
        return "redirect:/contact";
    }

    /**
     * POST /contact/submit-ajax  (used by the JavaScript on the contact page)
     *
     * Returns JSON instead of a page so the browser can show a toast
     * notification without reloading. The response body has the shape
     *   { "success": true,  "message": "..." }
     *   { "success": false, "message": "first field error" }
     */
    @PostMapping(value = "/contact/submit-ajax", produces = "application/json")
    public ResponseEntity<Map<String, Object>> submitContactAjax(
            @Valid @ModelAttribute ContactMessage message,
            BindingResult bindingResult) {

        Map<String, Object> body = new HashMap<>();
        if (bindingResult.hasErrors()) {
            body.put("success", false);
            body.put("message", bindingResult.getFieldErrors().get(0).getDefaultMessage());
            return ResponseEntity.badRequest().body(body);
        }
        contactMessageService.saveMessage(message);
        body.put("success", true);
        body.put("message", "Thank you! Your message has been sent successfully.");
        return ResponseEntity.ok(body);
    }

    // =====================================================================
    //  SMALL HELPERS
    // =====================================================================

    /**
     * The statistics shown in the About section. They are read live from the
     * database, so they update automatically when the admin adds something.
     */
    private Map<String, Long> buildPublicStats() {
        DashboardStats stats = dashboardService.getStats();
        Map<String, Long> publicStats = new HashMap<>();
        publicStats.put("projects", stats.totalProjects());
        publicStats.put("skills", stats.totalSkills());
        publicStats.put("certifications", stats.totalCertifications());
        publicStats.put("achievements", stats.totalAchievements());
        publicStats.put("experiences", stats.totalExperiences());
        publicStats.put("hackathons", achievementService.countHackathons());
        return publicStats;
    }

    /** "a, b, c" -> [a, b, c] with blanks removed. */
    private List<String> splitWords(String csv) {
        if (csv == null || csv.isBlank()) {
            return List.of();
        }
        return java.util.Arrays.stream(csv.split(","))
                .map(String::trim)
                .filter(word -> !word.isEmpty())
                .toList();
    }

    /** First {@code limit} items of a list - used for the home page previews. */
    private <T> List<T> take(List<T> items, int limit) {
        return items.size() <= limit ? items : items.subList(0, limit);
    }
}

```

---

## `portfolio-app/src/main/java/com/portfolio/controller/AuthController.java`
<a id="portfolio-app-src-main-java-com-portfolio-controller-authcontrollerjava"></a>

```java
package com.portfolio.controller;

import com.portfolio.dto.RegisterForm;
import com.portfolio.entity.AdminUser;
import com.portfolio.security.AuthHelper;
import com.portfolio.service.UserService;
import jakarta.validation.Valid;
import org.springframework.stereotype.Controller;
import org.springframework.ui.Model;
import org.springframework.validation.BindingResult;
import org.springframework.web.bind.annotation.GetMapping;
import org.springframework.web.bind.annotation.ModelAttribute;
import org.springframework.web.bind.annotation.PostMapping;
import org.springframework.web.bind.annotation.RequestParam;
import org.springframework.web.servlet.mvc.support.RedirectAttributes;

/**
 * ============================================================================
 * CONTROLLER : AuthController
 * ============================================================================
 * Handles user login (/login) and user registration (/register).
 * ============================================================================
 */
@Controller
public class AuthController {

    private final UserService userService;
    private final AuthHelper authHelper;

    public AuthController(UserService userService, AuthHelper authHelper) {
        this.userService = userService;
        this.authHelper = authHelper;
    }

    /**
     * Renders the login page.
     */
    @GetMapping("/login")
    public String loginPage(@RequestParam(value = "error", required = false) String error,
                            @RequestParam(value = "logout", required = false) String logout,
                            @RequestParam(value = "registered", required = false) String registered,
                            Model model) {
        if (authHelper.isAuthenticated()) {
            return "redirect:/admin/dashboard";
        }
        model.addAttribute("hasError", error != null);
        model.addAttribute("hasLogout", logout != null);
        model.addAttribute("hasRegistered", registered != null);
        return "auth/login";
    }



    /**
     * Renders the registration form.
     */
    @GetMapping("/register")
    public String registerPage(Model model) {
        if (authHelper.isAuthenticated()) {
            return "redirect:/admin/dashboard";
        }
        if (!model.containsAttribute("registerForm")) {
            model.addAttribute("registerForm", new RegisterForm());
        }
        return "auth/register";
    }

    /**
     * Processes registration form submission.
     */
    @PostMapping("/register")
    public String processRegistration(@Valid @ModelAttribute("registerForm") RegisterForm form,
                                      BindingResult bindingResult,
                                      RedirectAttributes redirectAttributes,
                                      Model model) {
        // Password confirmation check
        if (!form.isPasswordMatching()) {
            bindingResult.rejectValue("confirmPassword", "error.registerForm", "Passwords do not match.");
        }

        if (bindingResult.hasErrors()) {
            return "auth/register";
        }

        try {
            AdminUser user = userService.registerUser(form);
            redirectAttributes.addFlashAttribute("successMessage",
                    "Welcome, " + user.getFullName() + "! Your portfolio has been created. Please sign in below.");
            return "redirect:/login?registered=true";
        } catch (IllegalArgumentException ex) {
            model.addAttribute("errorMessage", ex.getMessage());
            return "auth/register";
        }
    }
}

```

---

## `portfolio-app/src/main/java/com/portfolio/controller/ExploreController.java`
<a id="portfolio-app-src-main-java-com-portfolio-controller-explorecontrollerjava"></a>

```java
package com.portfolio.controller;

import com.portfolio.entity.AdminUser;
import com.portfolio.service.ProjectService;
import com.portfolio.service.SkillService;
import com.portfolio.service.UserService;
import org.springframework.stereotype.Controller;
import org.springframework.ui.Model;
import org.springframework.web.bind.annotation.GetMapping;
import org.springframework.web.bind.annotation.RequestParam;

import java.util.ArrayList;
import java.util.HashMap;
import java.util.List;
import java.util.Map;

/**
 * ============================================================================
 * CONTROLLER : ExploreController
 * ============================================================================
 * Public community directory at /explore where visitors can browse different
 * registered user portfolios.
 * ============================================================================
 */
@Controller
public class ExploreController {

    private final UserService userService;
    private final ProjectService projectService;
    private final SkillService skillService;

    public ExploreController(UserService userService,
                             ProjectService projectService,
                             SkillService skillService) {
        this.userService = userService;
        this.projectService = projectService;
        this.skillService = skillService;
    }

    @GetMapping("/explore")
    public String explore(@RequestParam(value = "keyword", required = false) String keyword,
                          Model model) {
        List<AdminUser> users = userService.searchPublicUsers(keyword);
        List<Map<String, Object>> creatorCards = new ArrayList<>();

        for (AdminUser u : users) {
            Map<String, Object> card = new HashMap<>();
            card.put("user", u);
            card.put("projectCount", projectService.countPublic(u));
            card.put("skillCount", skillService.countAll(u));
            card.put("topSkills", skillService.getAllSkills(u).stream().limit(3).toList());
            creatorCards.add(card);
        }

        model.addAttribute("creators", creatorCards);
        model.addAttribute("users", users);
        model.addAttribute("keyword", keyword);
        model.addAttribute("totalCreators", users.size());
        model.addAttribute("activeSection", "explore");
        return "public/explore";
    }
}

```

---

## `portfolio-app/src/main/java/com/portfolio/controller/ResumeController.java`
<a id="portfolio-app-src-main-java-com-portfolio-controller-resumecontrollerjava"></a>

```java
package com.portfolio.controller;

import org.springframework.core.io.ClassPathResource;
import org.springframework.core.io.Resource;
import org.springframework.http.HttpHeaders;
import org.springframework.http.MediaType;
import org.springframework.http.ResponseEntity;
import org.springframework.stereotype.Controller;
import org.springframework.web.bind.annotation.GetMapping;

import java.io.IOException;

/**
 * ============================================================================
 * CONTROLLER : ResumeController  (the "Download Resume" button)
 * ============================================================================
 * GET /resume streams the resume PDF to the browser with a
 * {@code Content-Disposition: attachment} header, which makes Chrome / Edge /
 * Firefox open the "Save file" dialog instead of showing the PDF inline.
 *
 * ---------------------------------------------------------------------------
 * WHERE TO PUT YOUR RESUME PDF
 * ---------------------------------------------------------------------------
 *   src/main/resources/static/files/YourName-Resume.pdf
 *
 * The classpath location below ("static/files/portfolio-resume.pdf") is the
 * default. Either
 *   (a) name your file portfolio-resume.pdf, or
 *   (b) set app.resume.file=static/files/YourName-Resume.pdf in
 *       application.properties.
 *
 * After running "mvn clean package" the file ends up inside the jar, so it is
 * served from the packaged application too.
 * ============================================================================
 */
@Controller
public class ResumeController {

    @org.springframework.beans.factory.annotation.Value(
            "${app.resume.file:static/files/portfolio-resume.pdf}")
    private String resumeLocation;

    @GetMapping("/resume")
    public ResponseEntity<Resource> downloadResume() throws IOException {
        Resource resource = new ClassPathResource(resumeLocation);

        if (!resource.exists() || !resource.isReadable()) {
            // A friendly plain-text response instead of a stack trace, so the
            // student immediately knows the PDF is simply missing.
            return ResponseEntity.status(404)
                    .contentType(MediaType.TEXT_PLAIN)
                    .body(new org.springframework.core.io.ByteArrayResource(
                            ("Resume file not found.\n\n"
                                    + "Place your PDF at: src/main/resources/" + resumeLocation
                                    + "\nThen rebuild and restart the application.")
                                    .getBytes(java.nio.charset.StandardCharsets.UTF_8)));
        }

        String downloadName = resource.getFilename() == null
                ? "resume.pdf" : resource.getFilename();

        return ResponseEntity.ok()
                .contentType(MediaType.APPLICATION_PDF)
                .header(HttpHeaders.CONTENT_DISPOSITION,
                        "attachment; filename=\"" + downloadName + "\"")
                .body(resource);
    }
}

```

---

## `portfolio-app/src/main/java/com/portfolio/controller/UserPortfolioController.java`
<a id="portfolio-app-src-main-java-com-portfolio-controller-userportfoliocontrollerjava"></a>

```java
package com.portfolio.controller;

import com.portfolio.entity.AdminUser;
import com.portfolio.entity.ContactMessage;
import com.portfolio.entity.Project;
import com.portfolio.entity.ProjectCategory;
import com.portfolio.exception.ResourceNotFoundException;
import com.portfolio.service.AchievementService;
import com.portfolio.service.CertificationService;
import com.portfolio.service.ContactMessageService;
import com.portfolio.service.EducationService;
import com.portfolio.service.ExperienceService;
import com.portfolio.service.ProjectService;
import com.portfolio.service.SiteSettingService;
import com.portfolio.service.SkillService;
import com.portfolio.service.UserService;
import jakarta.validation.Valid;
import org.springframework.core.io.ByteArrayResource;
import org.springframework.core.io.ClassPathResource;
import org.springframework.core.io.Resource;
import org.springframework.http.HttpHeaders;
import org.springframework.http.MediaType;
import org.springframework.http.ResponseEntity;
import org.springframework.stereotype.Controller;
import org.springframework.ui.Model;
import org.springframework.validation.BindingResult;
import org.springframework.web.bind.annotation.GetMapping;
import org.springframework.web.bind.annotation.ModelAttribute;
import org.springframework.web.bind.annotation.PathVariable;
import org.springframework.web.bind.annotation.PostMapping;
import org.springframework.web.bind.annotation.RequestMapping;
import org.springframework.web.bind.annotation.RequestParam;
import org.springframework.web.bind.annotation.ResponseBody;
import org.springframework.web.servlet.mvc.support.RedirectAttributes;

import java.nio.charset.StandardCharsets;
import java.util.HashMap;
import java.util.List;
import java.util.Map;

/**
 * ============================================================================
 * CONTROLLER : UserPortfolioController
 * ============================================================================
 * Handles public viewing for any registered user's personal portfolio under
 * the route /u/{username}/**
 * ============================================================================
 */
@Controller
@RequestMapping("/u/{username}")
public class UserPortfolioController {

    private final UserService userService;
    private final ProjectService projectService;
    private final SkillService skillService;
    private final ExperienceService experienceService;
    private final EducationService educationService;
    private final CertificationService certificationService;
    private final AchievementService achievementService;
    private final SiteSettingService siteSettingService;
    private final ContactMessageService contactMessageService;

    public UserPortfolioController(UserService userService,
                                   ProjectService projectService,
                                   SkillService skillService,
                                   ExperienceService experienceService,
                                   EducationService educationService,
                                   CertificationService certificationService,
                                   AchievementService achievementService,
                                   SiteSettingService siteSettingService,
                                   ContactMessageService contactMessageService) {
        this.userService = userService;
        this.projectService = projectService;
        this.skillService = skillService;
        this.experienceService = experienceService;
        this.educationService = educationService;
        this.certificationService = certificationService;
        this.achievementService = achievementService;
        this.siteSettingService = siteSettingService;
        this.contactMessageService = contactMessageService;
    }

    private AdminUser loadUser(String username) {
        return userService.findByUsername(username)
                .orElseThrow(() -> new ResourceNotFoundException("Portfolio not found for user: @" + username));
    }

    private void populateUserContext(AdminUser user, Model model) {
        model.addAttribute("portfolioUser", user);
        model.addAttribute("settings", siteSettingService.getSettingsMap(user));
        model.addAttribute("userPrefix", "/u/" + user.getUsername());
        model.addAttribute("basePrefix", "/u/" + user.getUsername());
        model.addAttribute("services", siteSettingService.getServices(user));
    }

    // =====================================================================
    //  HOME / LANDING
    // =====================================================================

    @GetMapping
    public String userHome(@PathVariable String username, Model model) {
        AdminUser user = loadUser(username);
        populateUserContext(user, model);

        Map<String, Long> stats = new HashMap<>();
        stats.put("projects", projectService.countPublic(user));
        stats.put("skills", skillService.countAll(user));
        stats.put("certifications", certificationService.countAll(user));
        stats.put("hackathons", achievementService.countHackathons(user));
        model.addAttribute("stats", stats);

        model.addAttribute("projects", projectService.getPublicProjects(user).stream().limit(6).toList());
        model.addAttribute("skills", skillService.getAllSkills(user).stream().limit(6).toList());

        List<String> typingWords = List.of(
                user.getHeadline() != null ? user.getHeadline() : "Software Developer",
                "Web Applications",
                "Problem Solver"
        );
        model.addAttribute("typingWords", typingWords);
        model.addAttribute("activeSection", "home");
        return "public/index";
    }

    // =====================================================================
    //  ABOUT
    // =====================================================================

    @GetMapping("/about")
    public String userAbout(@PathVariable String username, Model model) {
        AdminUser user = loadUser(username);
        populateUserContext(user, model);

        Map<String, Long> stats = new HashMap<>();
        stats.put("projects", projectService.countPublic(user));
        stats.put("skills", skillService.countAll(user));
        stats.put("certifications", certificationService.countAll(user));
        stats.put("hackathons", achievementService.countHackathons(user));
        model.addAttribute("stats", stats);

        model.addAttribute("topSkills", skillService.getAllSkills(user).stream().limit(5).toList());
        model.addAttribute("activeSection", "about");
        return "public/about";
    }

    // =====================================================================
    //  SKILLS
    // =====================================================================

    @GetMapping("/skills")
    public String userSkills(@PathVariable String username, Model model) {
        AdminUser user = loadUser(username);
        populateUserContext(user, model);

        model.addAttribute("groupedSkills", skillService.getSkillsGroupedByCategory(user));
        model.addAttribute("totalSkills", skillService.countAll(user));
        model.addAttribute("activeSection", "skills");
        return "public/skills";
    }

    // =====================================================================
    //  PROJECTS
    // =====================================================================

    @GetMapping("/projects")
    public String userProjects(@PathVariable String username,
                               @RequestParam(value = "category", required = false) ProjectCategory category,
                               @RequestParam(value = "keyword", required = false) String keyword,
                               Model model) {
        AdminUser user = loadUser(username);
        populateUserContext(user, model);

        List<Project> list;
        if (keyword != null && !keyword.isBlank()) {
            list = projectService.searchProjects(user, keyword);
        } else {
            list = projectService.getPublicProjectsByCategory(user, category);
        }

        model.addAttribute("projects", list);
        model.addAttribute("categories", projectService.getAvailableCategories(user));
        model.addAttribute("selectedCategory", category);
        model.addAttribute("totalProjects", projectService.countPublic(user));
        model.addAttribute("keyword", keyword);
        model.addAttribute("activeSection", "projects");
        return "public/projects";
    }

    @GetMapping("/projects/{id}")
    public String userProjectDetails(@PathVariable String username,
                                     @PathVariable Long id,
                                     Model model) {
        AdminUser user = loadUser(username);
        populateUserContext(user, model);

        Project project = projectService.getProjectByIdAndUser(id, user);
        model.addAttribute("project", project);

        List<Project> related = projectService.getPublicProjects(user).stream()
                .filter(p -> !p.getId().equals(id))
                .limit(3)
                .toList();
        model.addAttribute("relatedProjects", related);
        model.addAttribute("activeSection", "projects");
        return "public/project-details";
    }

    // =====================================================================
    //  EDUCATION / EXPERIENCE / CERTIFICATIONS / ACHIEVEMENTS / SERVICES
    // =====================================================================

    @GetMapping("/education")
    public String userEducation(@PathVariable String username, Model model) {
        AdminUser user = loadUser(username);
        populateUserContext(user, model);
        model.addAttribute("educations", educationService.getAll(user));
        model.addAttribute("activeSection", "education");
        return "public/education";
    }

    @GetMapping("/experience")
    public String userExperience(@PathVariable String username, Model model) {
        AdminUser user = loadUser(username);
        populateUserContext(user, model);
        model.addAttribute("experiences", experienceService.getAll(user));
        model.addAttribute("activeSection", "experience");
        return "public/experience";
    }

    @GetMapping("/certifications")
    public String userCertifications(@PathVariable String username, Model model) {
        AdminUser user = loadUser(username);
        populateUserContext(user, model);
        model.addAttribute("certifications", certificationService.getAll(user));
        model.addAttribute("activeSection", "certifications");
        return "public/certifications";
    }

    @GetMapping("/achievements")
    public String userAchievements(@PathVariable String username, Model model) {
        AdminUser user = loadUser(username);
        populateUserContext(user, model);
        model.addAttribute("achievements", achievementService.getAll(user));
        model.addAttribute("activeSection", "achievements");
        return "public/achievements";
    }

    @GetMapping("/services")
    public String userServices(@PathVariable String username, Model model) {
        AdminUser user = loadUser(username);
        populateUserContext(user, model);
        model.addAttribute("activeSection", "services");
        return "public/services";
    }

    // =====================================================================
    //  CONTACT & MESSAGING
    // =====================================================================

    @GetMapping("/contact")
    public String userContact(@PathVariable String username, Model model) {
        AdminUser user = loadUser(username);
        populateUserContext(user, model);

        if (!model.containsAttribute("contactMessage")) {
            model.addAttribute("contactMessage", new ContactMessage());
        }
        model.addAttribute("contactAction", "/u/" + user.getUsername() + "/contact/submit");
        model.addAttribute("contactAjaxAction", "/u/" + user.getUsername() + "/contact/submit-ajax");
        model.addAttribute("activeSection", "contact");
        return "public/contact";
    }

    @PostMapping("/contact/submit")
    public String submitUserContact(@PathVariable String username,
                                    @Valid @ModelAttribute("contactMessage") ContactMessage message,
                                    BindingResult bindingResult,
                                    RedirectAttributes redirectAttributes,
                                    Model model) {
        AdminUser user = loadUser(username);
        if (bindingResult.hasErrors()) {
            populateUserContext(user, model);
            model.addAttribute("contactAction", "/u/" + user.getUsername() + "/contact/submit");
            model.addAttribute("contactAjaxAction", "/u/" + user.getUsername() + "/contact/submit-ajax");
            model.addAttribute("activeSection", "contact");
            return "public/contact";
        }

        message.setRecipient(user);
        contactMessageService.saveMessage(message);

        redirectAttributes.addFlashAttribute("successMessage",
                "Thank you, " + message.getName() + "! Your message was sent to " + user.getFullName() + ".");
        return "redirect:/u/" + user.getUsername() + "/contact";
    }

    @PostMapping(value = "/contact/submit-ajax", produces = "application/json")
    @ResponseBody
    public Map<String, Object> submitUserContactAjax(@PathVariable String username,
                                                    @Valid @ModelAttribute("contactMessage") ContactMessage message,
                                                    BindingResult bindingResult) {
        AdminUser user = loadUser(username);
        if (bindingResult.hasErrors()) {
            String firstError = bindingResult.getAllErrors().get(0).getDefaultMessage();
            return Map.of("success", false, "message", firstError != null ? firstError : "Invalid input.");
        }

        message.setRecipient(user);
        contactMessageService.saveMessage(message);

        return Map.of("success", true, "message",
                "Thank you, " + message.getName() + "! Your message has been delivered to " + user.getFullName() + ".");
    }

    // =====================================================================
    //  RESUME PDF
    // =====================================================================

    @GetMapping("/resume")
    public ResponseEntity<Resource> downloadUserResume(@PathVariable String username) {
        AdminUser user = loadUser(username);

        Resource resource = new ClassPathResource("static/files/" + user.getUsername() + "-resume.pdf");
        if (!resource.exists() || !resource.isReadable()) {
            resource = new ClassPathResource("static/files/portfolio-resume.pdf");
        }

        if (!resource.exists() || !resource.isReadable()) {
            return ResponseEntity.status(404)
                    .contentType(MediaType.TEXT_PLAIN)
                    .body(new ByteArrayResource(("Resume file not found for user @" + user.getUsername()).getBytes(StandardCharsets.UTF_8)));
        }

        return ResponseEntity.ok()
                .header(HttpHeaders.CONTENT_DISPOSITION, "attachment; filename=\"" + user.getUsername() + "-resume.pdf\"")
                .contentType(MediaType.APPLICATION_PDF)
                .body(resource);
    }
}

```

---

# 10. Admin Web Controllers

## `portfolio-app/src/main/java/com/portfolio/controller/admin/AdminAchievementController.java`
<a id="portfolio-app-src-main-java-com-portfolio-controller-admin-adminachievementcontrollerjava"></a>

```java
package com.portfolio.controller.admin;

import com.portfolio.entity.Achievement;
import com.portfolio.service.AchievementService;
import jakarta.validation.Valid;
import org.springframework.stereotype.Controller;
import org.springframework.ui.Model;
import org.springframework.validation.BindingResult;
import org.springframework.web.bind.annotation.GetMapping;
import org.springframework.web.bind.annotation.ModelAttribute;
import org.springframework.web.bind.annotation.PathVariable;
import org.springframework.web.bind.annotation.PostMapping;
import org.springframework.web.bind.annotation.RequestMapping;
import org.springframework.web.bind.annotation.RequestParam;
import org.springframework.web.servlet.mvc.support.RedirectAttributes;

/**
 * ============================================================================
 * CONTROLLER : AdminAchievementController  (CRUD for achievements)
 * ============================================================================
 */
@Controller
@RequestMapping("/admin/achievements")
public class AdminAchievementController {

    /** Category options offered in the form's select box. */
    private static final String[] CATEGORIES =
            {"Hackathon", "Competition", "Award", "Academic", "Other"};

    private final AchievementService achievementService;
    private final com.portfolio.security.AuthHelper authHelper;

    public AdminAchievementController(AchievementService achievementService,
                                      com.portfolio.security.AuthHelper authHelper) {
        this.achievementService = achievementService;
        this.authHelper = authHelper;
    }

    /** Makes CATEGORIES available to every template rendered by this controller. */
    @ModelAttribute("achievementCategories")
    public String[] categories() {
        return CATEGORIES;
    }

    /** LIST */
    @GetMapping
    public String list(@RequestParam(value = "keyword", required = false) String keyword,
                       Model model) {
        com.portfolio.entity.AdminUser user = authHelper.getCurrentUser();
        model.addAttribute("achievements", achievementService.search(user, keyword));
        model.addAttribute("keyword", keyword);
        model.addAttribute("activePage", "achievements");
        return "admin/achievement-list";
    }

    /** CREATE FORM */
    @GetMapping("/new")
    public String createForm(Model model) {
        model.addAttribute("achievement", new Achievement());
        model.addAttribute("pageTitle", "Add Achievement");
        model.addAttribute("activePage", "achievements");
        return "admin/achievement-form";
    }

    /** EDIT FORM */
    @GetMapping("/edit/{id}")
    public String editForm(@PathVariable Long id, Model model) {
        com.portfolio.entity.AdminUser user = authHelper.getCurrentUser();
        model.addAttribute("achievement", achievementService.getByIdAndUser(id, user));
        model.addAttribute("pageTitle", "Edit Achievement");
        model.addAttribute("activePage", "achievements");
        return "admin/achievement-form";
    }

    /** SAVE (create or update) */
    @PostMapping("/save")
    public String save(@Valid @ModelAttribute("achievement") Achievement achievement,
                       BindingResult bindingResult,
                       Model model,
                       RedirectAttributes redirectAttributes) {
        com.portfolio.entity.AdminUser user = authHelper.getCurrentUser();
        if (bindingResult.hasErrors()) {
            model.addAttribute("pageTitle",
                    achievement.getId() == null ? "Add Achievement" : "Edit Achievement");
            model.addAttribute("activePage", "achievements");
            return "admin/achievement-form";
        }
        boolean isNew = achievement.getId() == null;
        if (!isNew) {
            achievementService.getByIdAndUser(achievement.getId(), user);
        }
        achievement.setUser(user);
        achievementService.save(achievement);
        redirectAttributes.addFlashAttribute("successMessage",
                isNew ? "Achievement added successfully." : "Achievement updated successfully.");
        return "redirect:/admin/achievements";
    }

    /** DELETE */
    @PostMapping("/delete/{id}")
    public String delete(@PathVariable Long id, RedirectAttributes redirectAttributes) {
        com.portfolio.entity.AdminUser user = authHelper.getCurrentUser();
        achievementService.getByIdAndUser(id, user);
        achievementService.delete(id);
        redirectAttributes.addFlashAttribute("successMessage", "Achievement deleted successfully.");
        return "redirect:/admin/achievements";
    }
}

```

---

## `portfolio-app/src/main/java/com/portfolio/controller/admin/AdminCertificationController.java`
<a id="portfolio-app-src-main-java-com-portfolio-controller-admin-admincertificationcontrollerjava"></a>

```java
package com.portfolio.controller.admin;

import com.portfolio.entity.Certification;
import com.portfolio.service.CertificationService;
import com.portfolio.service.FileStorageService;
import jakarta.validation.Valid;
import org.springframework.stereotype.Controller;
import org.springframework.ui.Model;
import org.springframework.validation.BindingResult;
import org.springframework.web.bind.annotation.GetMapping;
import org.springframework.web.bind.annotation.ModelAttribute;
import org.springframework.web.bind.annotation.PathVariable;
import org.springframework.web.bind.annotation.PostMapping;
import org.springframework.web.bind.annotation.RequestMapping;
import org.springframework.web.bind.annotation.RequestParam;
import org.springframework.web.multipart.MultipartFile;
import org.springframework.web.servlet.mvc.support.RedirectAttributes;

/**
 * ============================================================================
 * CONTROLLER : AdminCertificationController  (CRUD + file upload)
 * ============================================================================
 * The multipart form can carry a certificate IMAGE. The stored path is written
 * to the certificateUrl / imageUrl columns by FileStorageService.
 * ============================================================================
 */
@Controller
@RequestMapping("/admin/certifications")
public class AdminCertificationController {

    private final CertificationService certificationService;
    private final FileStorageService fileStorageService;
    private final com.portfolio.security.AuthHelper authHelper;

    public AdminCertificationController(CertificationService certificationService,
                                        FileStorageService fileStorageService,
                                        com.portfolio.security.AuthHelper authHelper) {
        this.certificationService = certificationService;
        this.fileStorageService = fileStorageService;
        this.authHelper = authHelper;
    }

    /** LIST */
    @GetMapping
    public String list(@RequestParam(value = "keyword", required = false) String keyword,
                       Model model) {
        com.portfolio.entity.AdminUser user = authHelper.getCurrentUser();
        model.addAttribute("certifications", certificationService.search(user, keyword));
        model.addAttribute("keyword", keyword);
        model.addAttribute("activePage", "certifications");
        return "admin/certification-list";
    }

    /** CREATE FORM */
    @GetMapping("/new")
    public String createForm(Model model) {
        model.addAttribute("certification", new Certification());
        model.addAttribute("pageTitle", "Add Certification");
        model.addAttribute("activePage", "certifications");
        return "admin/certification-form";
    }

    /** EDIT FORM */
    @GetMapping("/edit/{id}")
    public String editForm(@PathVariable Long id, Model model) {
        com.portfolio.entity.AdminUser user = authHelper.getCurrentUser();
        model.addAttribute("certification", certificationService.getByIdAndUser(id, user));
        model.addAttribute("pageTitle", "Edit Certification");
        model.addAttribute("activePage", "certifications");
        return "admin/certification-form";
    }

    /** SAVE (create or update) with optional image upload */
    @PostMapping("/save")
    public String save(@Valid @ModelAttribute("certification") Certification certification,
                       BindingResult bindingResult,
                       @RequestParam(value = "imageFile", required = false) MultipartFile imageFile,
                       Model model,
                       RedirectAttributes redirectAttributes) {
        com.portfolio.entity.AdminUser user = authHelper.getCurrentUser();
        String title = certification.getId() == null ? "Add Certification" : "Edit Certification";

        if (bindingResult.hasErrors()) {
            model.addAttribute("pageTitle", title);
            model.addAttribute("activePage", "certifications");
            return "admin/certification-form";
        }

        try {
            boolean isNew = certification.getId() == null;
            if (!isNew) {
                certificationService.getByIdAndUser(certification.getId(), user);
            }
            certification.setUser(user);

            String uploadedUrl = fileStorageService.store(imageFile);
            if (uploadedUrl != null) {
                certification.setImageUrl(uploadedUrl);
                // If no explicit certificate link was given, the uploaded file
                // itself becomes the "View Certificate" target.
                if (certification.getCertificateUrl() == null
                        || certification.getCertificateUrl().isBlank()) {
                    certification.setCertificateUrl(uploadedUrl);
                }
            } else if (isNew && (certification.getImageUrl() == null
                    || certification.getImageUrl().isBlank())) {
                certification.setImageUrl("/img/certificate-placeholder.svg");
            }

            certificationService.save(certification);
            redirectAttributes.addFlashAttribute("successMessage",
                    isNew ? "Certification added successfully."
                          : "Certification updated successfully.");
        } catch (IllegalArgumentException ex) {
            // Thrown by FileStorageService for a wrong file type or size.
            bindingResult.rejectValue("imageUrl", "invalid", ex.getMessage());
            model.addAttribute("pageTitle", title);
            model.addAttribute("activePage", "certifications");
            return "admin/certification-form";
        }
        return "redirect:/admin/certifications";
    }

    /** DELETE */
    @PostMapping("/delete/{id}")
    public String delete(@PathVariable Long id, RedirectAttributes redirectAttributes) {
        com.portfolio.entity.AdminUser user = authHelper.getCurrentUser();
        certificationService.getByIdAndUser(id, user);
        certificationService.delete(id);
        redirectAttributes.addFlashAttribute("successMessage", "Certification deleted successfully.");
        return "redirect:/admin/certifications";
    }
}

```

---

## `portfolio-app/src/main/java/com/portfolio/controller/admin/AdminDashboardController.java`
<a id="portfolio-app-src-main-java-com-portfolio-controller-admin-admindashboardcontrollerjava"></a>

```java
package com.portfolio.controller.admin;

import com.portfolio.entity.Achievement;
import com.portfolio.entity.Certification;
import com.portfolio.entity.Education;
import com.portfolio.entity.Experience;
import com.portfolio.entity.Project;
import com.portfolio.entity.Skill;
import com.portfolio.service.AchievementService;
import com.portfolio.service.CertificationService;
import com.portfolio.service.ContactMessageService;
import com.portfolio.service.DashboardService;
import com.portfolio.service.EducationService;
import com.portfolio.service.ExperienceService;
import com.portfolio.service.ProjectService;
import com.portfolio.service.SkillService;
import org.springframework.stereotype.Controller;
import org.springframework.ui.Model;
import org.springframework.web.bind.annotation.GetMapping;
import org.springframework.web.bind.annotation.RequestMapping;

/**
 * ============================================================================
 * CONTROLLER : AdminDashboardController
 * ============================================================================
 * The first page after login. It shows the six counters plus the newest
 * entries of each table, so the admin gets an overview at a glance.
 *
 * PROTECTED BY SPRING SECURITY
 *   SecurityConfig maps /admin/** to hasRole("ADMIN"), so an anonymous
 *   visitor who types /admin/dashboard is redirected to /admin/login
 *   automatically - no check is needed in this class.
 * ============================================================================
 */
@Controller
@RequestMapping("/admin")
public class AdminDashboardController {

    private final DashboardService dashboardService;
    private final ProjectService projectService;
    private final SkillService skillService;
    private final EducationService educationService;
    private final ExperienceService experienceService;
    private final CertificationService certificationService;
    private final AchievementService achievementService;
    private final ContactMessageService contactMessageService;
    private final com.portfolio.security.AuthHelper authHelper;

    public AdminDashboardController(DashboardService dashboardService,
                                    ProjectService projectService,
                                    SkillService skillService,
                                    EducationService educationService,
                                    ExperienceService experienceService,
                                    CertificationService certificationService,
                                    AchievementService achievementService,
                                    ContactMessageService contactMessageService,
                                    com.portfolio.security.AuthHelper authHelper) {
        this.dashboardService = dashboardService;
        this.projectService = projectService;
        this.skillService = skillService;
        this.educationService = educationService;
        this.experienceService = experienceService;
        this.certificationService = certificationService;
        this.achievementService = achievementService;
        this.contactMessageService = contactMessageService;
        this.authHelper = authHelper;
    }

    /** GET /admin/dashboard */
    @GetMapping("/dashboard")
    public String dashboard(Model model) {
        com.portfolio.entity.AdminUser user = authHelper.getCurrentUser();
        model.addAttribute("stats", dashboardService.getStats(user));

        // Newest few rows of each table for current user
        model.addAttribute("recentProjects", limit(projectService.getAllProjects(user, null), 5));
        model.addAttribute("recentSkills", limit(skillService.getAllSkills(user), 5));
        model.addAttribute("recentEducations", limit(educationService.getAll(user), 3));
        model.addAttribute("recentExperiences", limit(experienceService.getAll(user), 3));
        model.addAttribute("recentCertifications", limit(certificationService.getAll(user), 3));
        model.addAttribute("recentAchievements", limit(achievementService.getAll(user), 3));
        model.addAttribute("recentMessages", limit(contactMessageService.getAllMessages(user), 5));
        model.addAttribute("portfolioUser", user);

        // Used by the sidebar to highlight the active menu item.
        model.addAttribute("activePage", "dashboard");
        return "admin/dashboard";
    }

    /** Keeps a list to at most {@code size} items. */
    private <T> java.util.List<T> limit(java.util.List<T> items, int size) {
        return items.size() <= size ? items : items.subList(0, size);
    }
}

```

---

## `portfolio-app/src/main/java/com/portfolio/controller/admin/AdminEducationController.java`
<a id="portfolio-app-src-main-java-com-portfolio-controller-admin-admineducationcontrollerjava"></a>

```java
package com.portfolio.controller.admin;

import com.portfolio.entity.Education;
import com.portfolio.service.EducationService;
import jakarta.validation.Valid;
import org.springframework.stereotype.Controller;
import org.springframework.ui.Model;
import org.springframework.validation.BindingResult;
import org.springframework.web.bind.annotation.GetMapping;
import org.springframework.web.bind.annotation.ModelAttribute;
import org.springframework.web.bind.annotation.PathVariable;
import org.springframework.web.bind.annotation.PostMapping;
import org.springframework.web.bind.annotation.RequestMapping;
import org.springframework.web.bind.annotation.RequestParam;
import org.springframework.web.servlet.mvc.support.RedirectAttributes;

/**
 * ============================================================================
 * CONTROLLER : AdminEducationController  (CRUD for education entries)
 * ============================================================================
 */
@Controller
@RequestMapping("/admin/education")
public class AdminEducationController {

    private final EducationService educationService;
    private final com.portfolio.security.AuthHelper authHelper;

    public AdminEducationController(EducationService educationService,
                                    com.portfolio.security.AuthHelper authHelper) {
        this.educationService = educationService;
        this.authHelper = authHelper;
    }

    /** LIST */
    @GetMapping
    public String list(@RequestParam(value = "keyword", required = false) String keyword,
                       Model model) {
        com.portfolio.entity.AdminUser user = authHelper.getCurrentUser();
        model.addAttribute("educations", educationService.search(user, keyword));
        model.addAttribute("keyword", keyword);
        model.addAttribute("activePage", "education");
        return "admin/education-list";
    }

    /** CREATE FORM */
    @GetMapping("/new")
    public String createForm(Model model) {
        Education education = new Education();
        education.setStartYear(java.time.Year.now().getValue() - 4);
        education.setEndYear(java.time.Year.now().getValue());
        model.addAttribute("education", education);
        model.addAttribute("pageTitle", "Add Education Entry");
        model.addAttribute("activePage", "education");
        return "admin/education-form";
    }

    /** EDIT FORM */
    @GetMapping("/edit/{id}")
    public String editForm(@PathVariable Long id, Model model) {
        com.portfolio.entity.AdminUser user = authHelper.getCurrentUser();
        model.addAttribute("education", educationService.getByIdAndUser(id, user));
        model.addAttribute("pageTitle", "Edit Education Entry");
        model.addAttribute("activePage", "education");
        return "admin/education-form";
    }

    /** SAVE (create or update) */
    @PostMapping("/save")
    public String save(@Valid @ModelAttribute("education") Education education,
                       BindingResult bindingResult,
                       Model model,
                       RedirectAttributes redirectAttributes) {
        com.portfolio.entity.AdminUser user = authHelper.getCurrentUser();
        if (bindingResult.hasErrors()) {
            model.addAttribute("pageTitle",
                    education.getId() == null ? "Add Education Entry" : "Edit Education Entry");
            model.addAttribute("activePage", "education");
            return "admin/education-form";
        }

        // Business rule from the service layer: end year >= start year.
        try {
            boolean isNew = education.getId() == null;
            if (!isNew) {
                // Ensure the user owns this education entry
                educationService.getByIdAndUser(education.getId(), user);
            }
            education.setUser(user);
            educationService.save(education);
            redirectAttributes.addFlashAttribute("successMessage",
                    isNew ? "Education entry added successfully."
                          : "Education entry updated successfully.");
        } catch (IllegalArgumentException ex) {
            bindingResult.rejectValue("endYear", "invalid", ex.getMessage());
            model.addAttribute("pageTitle",
                    education.getId() == null ? "Add Education Entry" : "Edit Education Entry");
            model.addAttribute("activePage", "education");
            return "admin/education-form";
        }
        return "redirect:/admin/education";
    }

    /** DELETE */
    @PostMapping("/delete/{id}")
    public String delete(@PathVariable Long id, RedirectAttributes redirectAttributes) {
        com.portfolio.entity.AdminUser user = authHelper.getCurrentUser();
        educationService.getByIdAndUser(id, user);
        educationService.delete(id);
        redirectAttributes.addFlashAttribute("successMessage", "Education entry deleted successfully.");
        return "redirect:/admin/education";
    }
}

```

---

## `portfolio-app/src/main/java/com/portfolio/controller/admin/AdminExperienceController.java`
<a id="portfolio-app-src-main-java-com-portfolio-controller-admin-adminexperiencecontrollerjava"></a>

```java
package com.portfolio.controller.admin;

import com.portfolio.entity.Experience;
import com.portfolio.service.ExperienceService;
import jakarta.validation.Valid;
import org.springframework.stereotype.Controller;
import org.springframework.ui.Model;
import org.springframework.validation.BindingResult;
import org.springframework.web.bind.annotation.GetMapping;
import org.springframework.web.bind.annotation.ModelAttribute;
import org.springframework.web.bind.annotation.PathVariable;
import org.springframework.web.bind.annotation.PostMapping;
import org.springframework.web.bind.annotation.RequestMapping;
import org.springframework.web.bind.annotation.RequestParam;
import org.springframework.web.servlet.mvc.support.RedirectAttributes;

/**
 * ============================================================================
 * CONTROLLER : AdminExperienceController  (CRUD for experience entries)
 * ============================================================================
 */
@Controller
@RequestMapping("/admin/experience")
public class AdminExperienceController {

    private final ExperienceService experienceService;
    private final com.portfolio.security.AuthHelper authHelper;

    public AdminExperienceController(ExperienceService experienceService,
                                     com.portfolio.security.AuthHelper authHelper) {
        this.experienceService = experienceService;
        this.authHelper = authHelper;
    }

    /** LIST */
    @GetMapping
    public String list(@RequestParam(value = "keyword", required = false) String keyword,
                       Model model) {
        com.portfolio.entity.AdminUser user = authHelper.getCurrentUser();
        model.addAttribute("experiences", experienceService.search(user, keyword));
        model.addAttribute("keyword", keyword);
        model.addAttribute("activePage", "experience");
        return "admin/experience-list";
    }

    /** CREATE FORM */
    @GetMapping("/new")
    public String createForm(Model model) {
        model.addAttribute("experience", new Experience());
        model.addAttribute("pageTitle", "Add Experience Entry");
        model.addAttribute("activePage", "experience");
        return "admin/experience-form";
    }

    /** EDIT FORM */
    @GetMapping("/edit/{id}")
    public String editForm(@PathVariable Long id, Model model) {
        com.portfolio.entity.AdminUser user = authHelper.getCurrentUser();
        model.addAttribute("experience", experienceService.getByIdAndUser(id, user));
        model.addAttribute("pageTitle", "Edit Experience Entry");
        model.addAttribute("activePage", "experience");
        return "admin/experience-form";
    }

    /** SAVE (create or update) */
    @PostMapping("/save")
    public String save(@Valid @ModelAttribute("experience") Experience experience,
                       BindingResult bindingResult,
                       Model model,
                       RedirectAttributes redirectAttributes) {
        com.portfolio.entity.AdminUser user = authHelper.getCurrentUser();
        String title = experience.getId() == null ? "Add Experience Entry" : "Edit Experience Entry";

        if (bindingResult.hasErrors()) {
            model.addAttribute("pageTitle", title);
            model.addAttribute("activePage", "experience");
            return "admin/experience-form";
        }

        try {
            experience.setUser(user);
            boolean isNew = experience.getId() == null;
            experienceService.save(experience);
            redirectAttributes.addFlashAttribute("successMessage",
                    isNew ? "Experience entry added successfully."
                          : "Experience entry updated successfully.");
        } catch (IllegalArgumentException ex) {
            bindingResult.rejectValue("endDate", "invalid", ex.getMessage());
            model.addAttribute("pageTitle", title);
            model.addAttribute("activePage", "experience");
            return "admin/experience-form";
        }
        return "redirect:/admin/experience";
    }

    /** DELETE */
    @PostMapping("/delete/{id}")
    public String delete(@PathVariable Long id, RedirectAttributes redirectAttributes) {
        com.portfolio.entity.AdminUser user = authHelper.getCurrentUser();
        experienceService.getByIdAndUser(id, user);
        experienceService.delete(id);
        redirectAttributes.addFlashAttribute("successMessage", "Experience entry deleted successfully.");
        return "redirect:/admin/experience";
    }
}

```

---

## `portfolio-app/src/main/java/com/portfolio/controller/admin/AdminLoginController.java`
<a id="portfolio-app-src-main-java-com-portfolio-controller-admin-adminlogincontrollerjava"></a>

```java
package com.portfolio.controller.admin;

import org.springframework.stereotype.Controller;
import org.springframework.ui.Model;
import org.springframework.web.bind.annotation.GetMapping;

/**
 * ============================================================================
 * CONTROLLER : AdminLoginController
 * ============================================================================
 * Only ONE job: show the login page at /admin/login.
 *
 * Notice what is NOT here - there is no code that checks the password.
 * The actual authentication is done by Spring Security, configured in
 * SecurityConfig:
 *
 *   GET  /admin/login  -> this method renders the form
 *   POST /admin/login  -> intercepted by Spring Security's
 *                         UsernamePasswordAuthenticationFilter, which calls
 *                         CustomUserDetailsService and the PasswordEncoder.
 *                         Success -> /admin/dashboard
 *                         Failure -> /admin/login?error=true
 *
 * That separation is the point: the application never handles a raw password.
 * ============================================================================
 */
@Controller
public class AdminLoginController {

    /**
     * Renders the login form.
     *
     * The two query parameters are added by Spring Security:
     *   ?error=true   -> wrong username or password
     *   ?logout=true  -> the admin just logged out
     * The template reads them from the request and shows the right alert.
     */
    @GetMapping("/admin/login")
    public String loginPage() {
        return "redirect:/login";
    }

    /**
     * A friendly landing page for /admin - simply forwards to the dashboard.
     * Keeps bookmarks to /admin working.
     */
    @GetMapping("/admin")
    public String adminRoot() {
        return "redirect:/admin/dashboard";
    }
}

```

---

## `portfolio-app/src/main/java/com/portfolio/controller/admin/AdminMessageController.java`
<a id="portfolio-app-src-main-java-com-portfolio-controller-admin-adminmessagecontrollerjava"></a>

```java
package com.portfolio.controller.admin;

import com.portfolio.entity.ContactMessage;
import com.portfolio.service.ContactMessageService;
import org.springframework.stereotype.Controller;
import org.springframework.ui.Model;
import org.springframework.web.bind.annotation.GetMapping;
import org.springframework.web.bind.annotation.PathVariable;
import org.springframework.web.bind.annotation.PostMapping;
import org.springframework.web.bind.annotation.RequestMapping;
import org.springframework.web.bind.annotation.RequestParam;
import org.springframework.web.servlet.mvc.support.RedirectAttributes;

/**
 * ============================================================================
 * CONTROLLER : AdminMessageController  (inbox for contact form submissions)
 * ============================================================================
 *   GET  /admin/messages                list (search + unread filter)
 *   GET  /admin/messages/view/{id}      open one message (also marks it read)
 *   POST /admin/messages/toggle/{id}    mark read / unread
 *   POST /admin/messages/delete/{id}    delete
 *   POST /admin/messages/delete-all-read delete every read message at once
 * ============================================================================
 */
@Controller
@RequestMapping("/admin/messages")
public class AdminMessageController {

    private final ContactMessageService contactMessageService;
    private final com.portfolio.security.AuthHelper authHelper;

    public AdminMessageController(ContactMessageService contactMessageService,
                                  com.portfolio.security.AuthHelper authHelper) {
        this.contactMessageService = contactMessageService;
        this.authHelper = authHelper;
    }

    /** LIST */
    @GetMapping
    public String list(@RequestParam(value = "keyword", required = false) String keyword,
                       @RequestParam(value = "unreadOnly", required = false) Boolean unreadOnly,
                       Model model) {
        com.portfolio.entity.AdminUser user = authHelper.getCurrentUser();
        java.util.List<ContactMessage> messages = contactMessageService.searchMessages(user, keyword);

        if (Boolean.TRUE.equals(unreadOnly)) {
            messages = messages.stream().filter(m -> !m.isReadStatus()).toList();
        }

        model.addAttribute("messages", messages);
        model.addAttribute("keyword", keyword);
        model.addAttribute("unreadOnly", Boolean.TRUE.equals(unreadOnly));
        model.addAttribute("unreadCount", contactMessageService.countUnread(user));
        model.addAttribute("totalCount", contactMessageService.countAll(user));
        model.addAttribute("activePage", "messages");
        return "admin/message-list";
    }

    /**
     * VIEW - opening a message marks it as read automatically, which is the
     * behaviour people expect from an inbox.
     */
    @GetMapping("/view/{id}")
    public String view(@PathVariable Long id, Model model) {
        com.portfolio.entity.AdminUser user = authHelper.getCurrentUser();
        ContactMessage message = contactMessageService.getMessageByIdAndRecipient(id, user);
        if (!message.isReadStatus()) {
            contactMessageService.markAsRead(id, true);
            message.setReadStatus(true);
        }
        model.addAttribute("message", message);
        model.addAttribute("activePage", "messages");
        return "admin/message-view";
    }

    /** MARK READ / UNREAD - one endpoint handles both directions. */
    @PostMapping("/toggle/{id}")
    public String toggleRead(@PathVariable Long id,
                             @RequestParam("read") boolean read,
                             RedirectAttributes redirectAttributes) {
        com.portfolio.entity.AdminUser user = authHelper.getCurrentUser();
        contactMessageService.getMessageByIdAndRecipient(id, user);
        contactMessageService.markAsRead(id, read);
        redirectAttributes.addFlashAttribute("successMessage",
                read ? "Message marked as read." : "Message marked as unread.");
        return "redirect:/admin/messages";
    }

    /** DELETE ONE */
    @PostMapping("/delete/{id}")
    public String delete(@PathVariable Long id, RedirectAttributes redirectAttributes) {
        com.portfolio.entity.AdminUser user = authHelper.getCurrentUser();
        contactMessageService.getMessageByIdAndRecipient(id, user);
        contactMessageService.deleteMessage(id);
        redirectAttributes.addFlashAttribute("successMessage", "Message deleted successfully.");
        return "redirect:/admin/messages";
    }

    /** DELETE ALL READ - a convenience action, guarded by a confirmation dialog. */
    @PostMapping("/delete-all-read")
    public String deleteAllRead(RedirectAttributes redirectAttributes) {
        com.portfolio.entity.AdminUser user = authHelper.getCurrentUser();
        long before = contactMessageService.countAll(user);
        contactMessageService.getAllMessages(user).stream()
                .filter(ContactMessage::isReadStatus)
                .map(ContactMessage::getId)
                .toList()
                .forEach(contactMessageService::deleteMessage);
        long removed = before - contactMessageService.countAll(user);
        redirectAttributes.addFlashAttribute("successMessage",
                removed + " read message(s) deleted.");
        return "redirect:/admin/messages";
    }
}

```

---

## `portfolio-app/src/main/java/com/portfolio/controller/admin/AdminProjectController.java`
<a id="portfolio-app-src-main-java-com-portfolio-controller-admin-adminprojectcontrollerjava"></a>

```java
package com.portfolio.controller.admin;

import com.portfolio.entity.Project;
import com.portfolio.entity.ProjectCategory;
import com.portfolio.service.FileStorageService;
import com.portfolio.service.ProjectService;
import jakarta.validation.Valid;
import org.springframework.stereotype.Controller;
import org.springframework.ui.Model;
import org.springframework.validation.BindingResult;
import org.springframework.web.bind.annotation.GetMapping;
import org.springframework.web.bind.annotation.ModelAttribute;
import org.springframework.web.bind.annotation.PathVariable;
import org.springframework.web.bind.annotation.PostMapping;
import org.springframework.web.bind.annotation.RequestMapping;
import org.springframework.web.bind.annotation.RequestParam;
import org.springframework.web.multipart.MultipartFile;
import org.springframework.web.servlet.mvc.support.RedirectAttributes;

/**
 * ============================================================================
 * CONTROLLER : AdminProjectController  (full CRUD for projects)
 * ============================================================================
 * URL PATTERN (a standard REST-ish convention, easy to explain)
 *   GET    /admin/projects            -> list      (Read)
 *   GET    /admin/projects/new        -> form      (Create - show)
 *   POST   /admin/projects/save       -> save      (Create - do it)
 *   GET    /admin/projects/edit/{id}  -> form      (Update - show)
 *   GET    /admin/projects/view/{id}  -> details   (Read one)
 *   POST   /admin/projects/delete/{id}-> delete    (Delete)
 *
 * DELETES USE POST, NOT GET
 *   A GET link can be triggered by a browser prefetch or a crawler. Using
 *   POST + a confirmation dialog means a record is only removed on purpose.
 * ============================================================================
 */
@Controller
@RequestMapping("/admin/projects")
public class AdminProjectController {

    private final ProjectService projectService;
    private final FileStorageService fileStorageService;
    private final com.portfolio.security.AuthHelper authHelper;

    public AdminProjectController(ProjectService projectService,
                                  FileStorageService fileStorageService,
                                  com.portfolio.security.AuthHelper authHelper) {
        this.projectService = projectService;
        this.fileStorageService = fileStorageService;
        this.authHelper = authHelper;
    }

    /** LIST - with optional category filter and keyword search for current user. */
    @GetMapping
    public String list(@RequestParam(value = "category", required = false) ProjectCategory category,
                       @RequestParam(value = "keyword", required = false) String keyword,
                       Model model) {
        com.portfolio.entity.AdminUser user = authHelper.getCurrentUser();
        if (keyword != null && !keyword.isBlank()) {
            model.addAttribute("projects", projectService.searchProjects(user, keyword));
        } else {
            model.addAttribute("projects", projectService.getAllProjects(user, category));
        }
        model.addAttribute("selectedCategory", category);
        model.addAttribute("keyword", keyword);
        model.addAttribute("activePage", "projects");
        return "admin/project-list";
    }

    /**
     * Makes the category list available to the form template without having to
     * repeat this line in every method that renders the form.
     */
    @ModelAttribute("categories")
    public ProjectCategory[] categories() {
        return ProjectCategory.values();
    }

    /** CREATE FORM - an empty Project object is bound to the form. */
    @GetMapping("/new")
    public String createForm(Model model) {
        model.addAttribute("project", new Project());
        model.addAttribute("pageTitle", "Add New Project");
        model.addAttribute("activePage", "projects");
        return "admin/project-form";
    }

    /** EDIT FORM - the existing row is loaded and pre-filled into the form. */
    @GetMapping("/edit/{id}")
    public String editForm(@PathVariable Long id, Model model) {
        com.portfolio.entity.AdminUser user = authHelper.getCurrentUser();
        model.addAttribute("project", projectService.getProjectByIdAndUser(id, user));
        model.addAttribute("pageTitle", "Edit Project");
        model.addAttribute("activePage", "projects");
        return "admin/project-form";
    }

    /**
     * VIEW - admin preview of the public details page.
     * Reuses the public template, which proves the same data drives both.
     */
    @GetMapping("/view/{id}")
    public String view(@PathVariable Long id, Model model) {
        com.portfolio.entity.AdminUser user = authHelper.getCurrentUser();
        model.addAttribute("project", projectService.getProjectByIdAndUser(id, user));
        model.addAttribute("relatedProjects", java.util.List.of());
        model.addAttribute("adminView", true);
        model.addAttribute("activeSection", "projects");
        return "public/project-details";
    }

    /**
     * SAVE - handles BOTH create and update.
     */
    @PostMapping("/save")
    public String save(@Valid @ModelAttribute("project") Project project,
                       BindingResult bindingResult,
                       @RequestParam(value = "imageFile", required = false) MultipartFile imageFile,
                       Model model,
                       RedirectAttributes redirectAttributes) {

        com.portfolio.entity.AdminUser user = authHelper.getCurrentUser();

        if (bindingResult.hasErrors()) {
            model.addAttribute("pageTitle",
                    project.getId() == null ? "Add New Project" : "Edit Project");
            model.addAttribute("activePage", "projects");
            return "admin/project-form";
        }

        // Upload the cover image when one was chosen.
        String uploadedUrl = fileStorageService.store(imageFile);
        if (uploadedUrl != null) {
            project.setImageUrl(uploadedUrl);
        } else if (project.getId() == null && (project.getImageUrl() == null || project.getImageUrl().isBlank())) {
            project.setImageUrl("/img/project-placeholder.svg");
        }

        project.setUser(user);
        boolean isNew = project.getId() == null;
        projectService.saveProject(project);

        redirectAttributes.addFlashAttribute("successMessage",
                isNew ? "Project added successfully." : "Project updated successfully.");
        return "redirect:/admin/projects";
    }

    /** DELETE - with a confirmation message back to the list. */
    @PostMapping("/delete/{id}")
    public String delete(@PathVariable Long id, RedirectAttributes redirectAttributes) {
        com.portfolio.entity.AdminUser user = authHelper.getCurrentUser();
        // Verify ownership
        projectService.getProjectByIdAndUser(id, user);
        projectService.deleteProject(id);
        redirectAttributes.addFlashAttribute("successMessage", "Project deleted successfully.");
        return "redirect:/admin/projects";
    }
}

```

---

## `portfolio-app/src/main/java/com/portfolio/controller/admin/AdminSettingsController.java`
<a id="portfolio-app-src-main-java-com-portfolio-controller-admin-adminsettingscontrollerjava"></a>

```java
package com.portfolio.controller.admin;

import com.portfolio.dto.ChangePasswordForm;
import com.portfolio.entity.AdminUser;
import com.portfolio.entity.SettingKey;
import com.portfolio.entity.SiteSetting;
import com.portfolio.repository.AdminUserRepository;
import com.portfolio.service.FileStorageService;
import com.portfolio.service.SiteSettingService;
import jakarta.validation.Valid;
import org.springframework.security.core.context.SecurityContextHolder;
import org.springframework.security.crypto.password.PasswordEncoder;
import org.springframework.stereotype.Controller;
import org.springframework.ui.Model;
import org.springframework.validation.BindingResult;
import org.springframework.web.bind.annotation.GetMapping;
import org.springframework.web.bind.annotation.ModelAttribute;
import org.springframework.web.bind.annotation.PostMapping;
import org.springframework.web.bind.annotation.RequestMapping;
import org.springframework.web.bind.annotation.RequestParam;
import org.springframework.web.multipart.MultipartFile;
import org.springframework.web.servlet.mvc.support.RedirectAttributes;

import java.util.Map;

/**
 * ============================================================================
 * CONTROLLER : AdminSettingsController
 * ============================================================================
 * Two screens under /admin/settings:
 *
 *   1. PROFILE  - every key/value in site_settings, so the admin can change
 *                 the name, title, intro, career objective, social links and
 *                 the "What I Do" services without touching code.
 *
 *   2. SECURITY - change the login password. The current password must be
 *                 entered again, and the new one is stored as a BCrypt hash.
 * ============================================================================
 */
@Controller
@RequestMapping("/admin/settings")
public class AdminSettingsController {

    private final SiteSettingService siteSettingService;
    private final AdminUserRepository adminUserRepository;
    private final PasswordEncoder passwordEncoder;
    private final FileStorageService fileStorageService;
    private final com.portfolio.security.AuthHelper authHelper;

    public AdminSettingsController(SiteSettingService siteSettingService,
                                   AdminUserRepository adminUserRepository,
                                   PasswordEncoder passwordEncoder,
                                   FileStorageService fileStorageService,
                                   com.portfolio.security.AuthHelper authHelper) {
        this.siteSettingService = siteSettingService;
        this.adminUserRepository = adminUserRepository;
        this.passwordEncoder = passwordEncoder;
        this.fileStorageService = fileStorageService;
        this.authHelper = authHelper;
    }

    // =====================================================================
    //  PROFILE SETTINGS
    // =====================================================================

    /** GET /admin/settings - the profile editor. */
    @GetMapping
    public String settingsPage(Model model) {
        AdminUser user = authHelper.getCurrentUser();
        model.addAttribute("settingList", siteSettingService.getAll(user));
        model.addAttribute("changePasswordForm", new ChangePasswordForm());
        model.addAttribute("activePage", "settings");
        return "admin/settings";
    }

    /**
     * POST /admin/settings/save
     *
     * The form posts every input under its setting key, so the map arrives as
     * { "hero.name" -> "Your Name", "about.email" -> "...", ... }.
     * Keys are checked against the SettingKey whitelist: only keys this
     * application actually knows about can be written. That prevents someone
     * from injecting arbitrary rows by adding a field to the HTML.
     */
    @PostMapping("/save")
    public String saveSettings(@RequestParam Map<String, String> allParams,
                               @RequestParam(value = "profileImageFile", required = false)
                               MultipartFile profileImageFile,
                               RedirectAttributes redirectAttributes) {
        AdminUser user = authHelper.getCurrentUser();
        java.util.Set<String> allowedKeys = java.util.Set.of(
                SettingKey.HERO_NAME, SettingKey.HERO_TITLE, SettingKey.HERO_INTRO,
                SettingKey.HERO_TYPING_WORDS, SettingKey.PROFILE_IMAGE, SettingKey.RESUME_URL,
                SettingKey.ABOUT_INTRO, SettingKey.ABOUT_OBJECTIVE, SettingKey.ABOUT_INTERESTS,
                SettingKey.ABOUT_DOB, SettingKey.ABOUT_EMAIL, SettingKey.ABOUT_PHONE,
                SettingKey.ABOUT_LOCATION, SettingKey.ABOUT_LANGUAGES,
                SettingKey.SOCIAL_GITHUB, SettingKey.SOCIAL_LINKEDIN,
                SettingKey.SOCIAL_TWITTER, SettingKey.SOCIAL_INSTAGRAM,
                SettingKey.SERVICES
        );

        int saved = 0;
        for (Map.Entry<String, String> entry : allParams.entrySet()) {
            if (allowedKeys.contains(entry.getKey())) {
                siteSettingService.saveValue(user, entry.getKey(), entry.getValue(), null);
                saved++;
            }
        }

        // Optional profile photo upload.
        String uploadedUrl = fileStorageService.store(profileImageFile);
        if (uploadedUrl != null) {
            siteSettingService.saveValue(user, SettingKey.PROFILE_IMAGE, uploadedUrl, "Profile Photo Path");
        }

        // Sync core AdminUser entity profile fields for Explore and User directory
        if (user != null) {
            if (allParams.containsKey(SettingKey.HERO_NAME) && !allParams.get(SettingKey.HERO_NAME).isBlank()) {
                user.setFullName(allParams.get(SettingKey.HERO_NAME).trim());
            }
            if (allParams.containsKey(SettingKey.HERO_TITLE) && !allParams.get(SettingKey.HERO_TITLE).isBlank()) {
                user.setHeadline(allParams.get(SettingKey.HERO_TITLE).trim());
            }
            if (allParams.containsKey(SettingKey.HERO_INTRO) && !allParams.get(SettingKey.HERO_INTRO).isBlank()) {
                user.setBio(allParams.get(SettingKey.HERO_INTRO).trim());
            }
            if (allParams.containsKey(SettingKey.ABOUT_LOCATION) && !allParams.get(SettingKey.ABOUT_LOCATION).isBlank()) {
                user.setLocation(allParams.get(SettingKey.ABOUT_LOCATION).trim());
            }
            if (allParams.containsKey(SettingKey.ABOUT_PHONE) && !allParams.get(SettingKey.ABOUT_PHONE).isBlank()) {
                user.setPhone(allParams.get(SettingKey.ABOUT_PHONE).trim());
            }
            if (allParams.containsKey(SettingKey.SOCIAL_GITHUB) && !allParams.get(SettingKey.SOCIAL_GITHUB).isBlank()) {
                user.setGithubUrl(allParams.get(SettingKey.SOCIAL_GITHUB).trim());
            }
            if (allParams.containsKey(SettingKey.SOCIAL_LINKEDIN) && !allParams.get(SettingKey.SOCIAL_LINKEDIN).isBlank()) {
                user.setLinkedinUrl(allParams.get(SettingKey.SOCIAL_LINKEDIN).trim());
            }
            if (allParams.containsKey(SettingKey.SOCIAL_TWITTER) && !allParams.get(SettingKey.SOCIAL_TWITTER).isBlank()) {
                user.setTwitterUrl(allParams.get(SettingKey.SOCIAL_TWITTER).trim());
            }
            if (uploadedUrl != null) {
                user.setAvatarUrl(uploadedUrl);
            }
            adminUserRepository.save(user);
        }

        redirectAttributes.addFlashAttribute("successMessage",
                "Profile updated (" + saved + " field(s) saved).");
        return "redirect:/admin/settings";
    }

    // =====================================================================
    //  CHANGE PASSWORD
    // =====================================================================

    /**
     * POST /admin/settings/change-password
     *
     * STEPS
     *   1. Bean validation on the form (length, matching confirmation)
     *   2. verify the CURRENT password with passwordEncoder.matches(...)
     *      - it compares against the stored BCrypt hash, never plain text
     *   3. hash the new password and save it
     *
     * The currently logged-in username comes from the SecurityContext, so it
     * cannot be spoofed from the form.
     */
    @PostMapping("/change-password")
    public String changePassword(@Valid @ModelAttribute("changePasswordForm") ChangePasswordForm form,
                                 BindingResult bindingResult,
                                 Model model,
                                 RedirectAttributes redirectAttributes) {
        AdminUser adminUser = authHelper.getCurrentUser();

        if (bindingResult.hasErrors()) {
            model.addAttribute("settingList", siteSettingService.getAll(adminUser));
            model.addAttribute("activePage", "settings");
            model.addAttribute("passwordTab", true);
            return "admin/settings";
        }

        if (adminUser == null) {
            bindingResult.rejectValue("currentPassword", "invalid",
                    "The logged-in account no longer exists.");
            model.addAttribute("settingList", siteSettingService.getAll(null));
            model.addAttribute("activePage", "settings");
            model.addAttribute("passwordTab", true);
            return "admin/settings";
        }

        // matches(rawPassword, encodedPassword) -> boolean
        if (!passwordEncoder.matches(form.getCurrentPassword(), adminUser.getPassword())) {
            bindingResult.rejectValue("currentPassword", "invalid",
                    "Your current password is incorrect.");
            model.addAttribute("settingList", siteSettingService.getAll(adminUser));
            model.addAttribute("activePage", "settings");
            model.addAttribute("passwordTab", true);
            return "admin/settings";
        }

        // Store the new BCrypt hash.
        adminUser.setPassword(passwordEncoder.encode(form.getNewPassword()));
        adminUserRepository.save(adminUser);

        redirectAttributes.addFlashAttribute("successMessage",
                "Password changed successfully. Use the new password next time you log in.");
        return "redirect:/admin/settings";
    }

}

```

---

## `portfolio-app/src/main/java/com/portfolio/controller/admin/AdminSkillController.java`
<a id="portfolio-app-src-main-java-com-portfolio-controller-admin-adminskillcontrollerjava"></a>

```java
package com.portfolio.controller.admin;

import com.portfolio.entity.Skill;
import com.portfolio.service.SkillService;
import jakarta.validation.Valid;
import org.springframework.stereotype.Controller;
import org.springframework.ui.Model;
import org.springframework.validation.BindingResult;
import org.springframework.web.bind.annotation.GetMapping;
import org.springframework.web.bind.annotation.ModelAttribute;
import org.springframework.web.bind.annotation.PathVariable;
import org.springframework.web.bind.annotation.PostMapping;
import org.springframework.web.bind.annotation.RequestMapping;
import org.springframework.web.bind.annotation.RequestParam;
import org.springframework.web.servlet.mvc.support.RedirectAttributes;

/**
 * ============================================================================
 * CONTROLLER : AdminSkillController  (full CRUD for skills)
 * ============================================================================
 * Same structure as the project controller:
 *   GET  /admin/skills             list (with search)
 *   GET  /admin/skills/new         create form
 *   GET  /admin/skills/edit/{id}   edit form
 *   POST /admin/skills/save        create or update
 *   POST /admin/skills/delete/{id} delete
 * ============================================================================
 */
@Controller
@RequestMapping("/admin/skills")
public class AdminSkillController {

    private final SkillService skillService;
    private final com.portfolio.security.AuthHelper authHelper;

    public AdminSkillController(SkillService skillService,
                                com.portfolio.security.AuthHelper authHelper) {
        this.skillService = skillService;
        this.authHelper = authHelper;
    }

    /** Existing category names - offered as suggestions in the form's datalist. */
    @ModelAttribute("existingCategories")
    public java.util.List<String> existingCategories() {
        return authHelper.getCurrentUserOptional()
                .map(skillService::getAllCategories)
                .orElseGet(skillService::getAllCategories);
    }

    /** LIST */
    @GetMapping
    public String list(@RequestParam(value = "keyword", required = false) String keyword,
                       Model model) {
        com.portfolio.entity.AdminUser user = authHelper.getCurrentUser();
        model.addAttribute("skills", skillService.searchSkills(user, keyword));
        model.addAttribute("keyword", keyword);
        model.addAttribute("totalSkills", skillService.countAll(user));
        model.addAttribute("activePage", "skills");
        return "admin/skill-list";
    }

    /** CREATE FORM */
    @GetMapping("/new")
    public String createForm(Model model) {
        Skill skill = new Skill();
        skill.setProficiency(75);   // a sensible starting value
        model.addAttribute("skill", skill);
        model.addAttribute("pageTitle", "Add New Skill");
        model.addAttribute("activePage", "skills");
        return "admin/skill-form";
    }

    /** EDIT FORM */
    @GetMapping("/edit/{id}")
    public String editForm(@PathVariable Long id, Model model) {
        com.portfolio.entity.AdminUser user = authHelper.getCurrentUser();
        model.addAttribute("skill", skillService.getSkillByIdAndUser(id, user));
        model.addAttribute("pageTitle", "Edit Skill");
        model.addAttribute("activePage", "skills");
        return "admin/skill-form";
    }

    /** SAVE (create or update) */
    @PostMapping("/save")
    public String save(@Valid @ModelAttribute("skill") Skill skill,
                       BindingResult bindingResult,
                       Model model,
                       RedirectAttributes redirectAttributes) {
        com.portfolio.entity.AdminUser user = authHelper.getCurrentUser();
        if (bindingResult.hasErrors()) {
            model.addAttribute("pageTitle",
                    skill.getId() == null ? "Add New Skill" : "Edit Skill");
            model.addAttribute("activePage", "skills");
            return "admin/skill-form";
        }
        skill.setUser(user);
        boolean isNew = skill.getId() == null;
        skillService.saveSkill(skill);
        redirectAttributes.addFlashAttribute("successMessage",
                isNew ? "Skill added successfully." : "Skill updated successfully.");
        return "redirect:/admin/skills";
    }

    /** DELETE */
    @PostMapping("/delete/{id}")
    public String delete(@PathVariable Long id, RedirectAttributes redirectAttributes) {
        com.portfolio.entity.AdminUser user = authHelper.getCurrentUser();
        skillService.getSkillByIdAndUser(id, user);
        skillService.deleteSkill(id);
        redirectAttributes.addFlashAttribute("successMessage", "Skill deleted successfully.");
        return "redirect:/admin/skills";
    }
}

```

---

# 11. Frontend Layout & Reusable Fragments

## `portfolio-app/src/main/resources/templates/fragments/admin-sidebar.html`
<a id="portfolio-app-src-main-resources-templates-fragments-admin-sidebarhtml"></a>

```html
<!DOCTYPE html>
<!--
  ============================================================================
  FRAGMENT : admin-sidebar
  ============================================================================
  Usage:  <aside th:replace="~{fragments/admin-sidebar :: sidebar}"></aside>

  The controller sets "activePage" and the matching link gets .active.
  "unreadMessages" is a global model attribute (GlobalModelAttributes), so the
  red badge on Messages always shows the current count.
  ============================================================================
-->
<html xmlns:th="http://www.thymeleaf.org"
      xmlns:sec="http://www.thymeleaf.org/extras/spring-security">
<body>

<aside th:fragment="sidebar" class="admin-sidebar" id="adminSidebar">

    <a th:href="@{/admin/dashboard}" class="sidebar-brand">
        <span class="brand-mark"><i class="bi bi-speedometer2"></i></span>
        <span>Admin Panel</span>
    </a>

    <div class="sidebar-label">Overview</div>
    <a th:href="@{/admin/dashboard}" class="sidebar-link"
       th:classappend="${activePage == 'dashboard'} ? 'active'">
        <span class="ico"><i class="bi bi-grid-1x2-fill"></i></span> Dashboard
    </a>

    <div class="sidebar-label">Content</div>

    <a th:href="@{/admin/projects}" class="sidebar-link"
       th:classappend="${activePage == 'projects'} ? 'active'">
        <span class="ico"><i class="bi bi-folder-fill"></i></span> Projects
    </a>

    <a th:href="@{/admin/skills}" class="sidebar-link"
       th:classappend="${activePage == 'skills'} ? 'active'">
        <span class="ico"><i class="bi bi-bar-chart-fill"></i></span> Skills
    </a>

    <a th:href="@{/admin/education}" class="sidebar-link"
       th:classappend="${activePage == 'education'} ? 'active'">
        <span class="ico"><i class="bi bi-mortarboard-fill"></i></span> Education
    </a>

    <a th:href="@{/admin/experience}" class="sidebar-link"
       th:classappend="${activePage == 'experience'} ? 'active'">
        <span class="ico"><i class="bi bi-briefcase-fill"></i></span> Experience
    </a>

    <a th:href="@{/admin/certifications}" class="sidebar-link"
       th:classappend="${activePage == 'certifications'} ? 'active'">
        <span class="ico"><i class="bi bi-patch-check-fill"></i></span> Certifications
    </a>

    <a th:href="@{/admin/achievements}" class="sidebar-link"
       th:classappend="${activePage == 'achievements'} ? 'active'">
        <span class="ico"><i class="bi bi-trophy-fill"></i></span> Achievements
    </a>

    <div class="sidebar-label">Inbox</div>
    <a th:href="@{/admin/messages}" class="sidebar-link"
       th:classappend="${activePage == 'messages'} ? 'active'">
        <span class="ico"><i class="bi bi-envelope-fill"></i></span> Messages
        <span class="count-pill" th:if="${unreadMessages > 0}" th:text="${unreadMessages}">0</span>
    </a>

    <div class="sidebar-label">Account</div>
    <a th:href="@{/admin/settings}" class="sidebar-link"
       th:classappend="${activePage == 'settings'} ? 'active'">
        <span class="ico"><i class="bi bi-gear-fill"></i></span> Settings
    </a>

    <div class="sidebar-footer">
        <a th:href="@{'/u/' + ${currentUser != null ? currentUser.username : 'admin'}}" class="sidebar-link" target="_blank">
            <span class="ico"><i class="bi bi-window-fullscreen"></i></span> My Portfolio
        </a>

        <a th:href="@{/explore}" class="sidebar-link" target="_blank">
            <span class="ico"><i class="bi bi-compass"></i></span> Explore Showcase
        </a>

        <!-- Logout is a POST (CSRF-protected), so it is a form, not a link -->
        <form th:action="@{/logout}" method="post"
              data-confirm="Do you really want to log out?"
              data-confirm-title="Log out">
            <button type="submit" class="sidebar-link" style="width:100%; border:none; text-align:left;">
                <span class="ico"><i class="bi bi-box-arrow-right"></i></span> Logout
            </button>
        </form>

        <div style="padding:10px 12px 0; font-size:.78rem; color:var(--text-muted);">
            Signed in as
            <strong th:text="${currentUser != null ? (currentUser.fullName != null and !currentUser.fullName.isBlank() ? currentUser.fullName : currentUser.username) : 'Admin'}"
                    style="color:var(--text-primary);">admin</strong>
        </div>
    </div>
</aside>

</body>
</html>

```

---

## `portfolio-app/src/main/resources/templates/fragments/admin-topbar.html`
<a id="portfolio-app-src-main-resources-templates-fragments-admin-topbarhtml"></a>

```html
<!DOCTYPE html>
<!--
  ============================================================================
  FRAGMENT : admin-topbar
  ============================================================================
  Usage:  <header th:replace="~{fragments/admin-topbar :: topbar('Page Title')}"></header>

  Contains the hamburger (mobile), the page title, the theme toggle and the
  shortcut buttons. It also holds the backdrop element that dims the page
  while the mobile sidebar drawer is open.
  ============================================================================
-->
<html xmlns:th="http://www.thymeleaf.org"
      xmlns:sec="http://www.thymeleaf.org/extras/spring-security">
<body>

<div th:fragment="topbar(title)">

    <header class="admin-topbar">
        <div class="gap-row">
            <button type="button" class="sidebar-toggle" id="sidebarToggle"
                    aria-label="Open menu"><i class="bi bi-list"></i></button>
            <h1 th:text="${title}">Dashboard</h1>
        </div>

        <div class="gap-row">
            <a th:href="@{'/u/' + ${currentUser != null ? currentUser.username : 'admin'}}" target="_blank" class="btn btn-ghost btn-sm"
               title="Open your personal portfolio in a new tab">
                <i class="bi bi-window-fullscreen"></i> My Portfolio
            </a>

            <a th:href="@{/explore}" target="_blank" class="btn btn-ghost btn-sm d-none d-md-inline-flex"
               title="Explore developer showcase">
                <i class="bi bi-compass"></i> Explore
            </a>

            <button type="button" class="icon-btn" id="themeToggle"
                    title="Toggle dark / light mode" aria-label="Toggle theme">
                <i class="bi bi-moon-stars-fill" id="themeIcon"></i>
            </button>

            <form th:action="@{/logout}" method="post" style="display:inline;"
                  data-confirm="Do you really want to log out?"
                  data-confirm-title="Log out">
                <button type="submit" class="btn btn-outline btn-sm" title="Log out">
                    <i class="bi bi-box-arrow-right"></i>
                    <span class="d-none d-sm-inline" th:text="' ' + (${currentUser != null ? currentUser.username : 'admin'})">admin</span>
                </button>
            </form>
        </div>
    </header>

    <!-- Dims the page behind the mobile sidebar -->
    <div class="sidebar-backdrop" id="sidebarBackdrop"></div>
</div>

</body>
</html>

```

---

## `portfolio-app/src/main/resources/templates/fragments/alerts.html`
<a id="portfolio-app-src-main-resources-templates-fragments-alertshtml"></a>

```html
<!DOCTYPE html>
<!--
  ============================================================================
  FRAGMENT : alerts
  ============================================================================
  Usage:  <div th:replace="~{fragments/alerts :: alerts}"></div>

  Shows the flash messages that controllers add with
      redirectAttributes.addFlashAttribute("successMessage", "...")
      redirectAttributes.addFlashAttribute("errorMessage",   "...")

  Flash attributes survive exactly ONE redirect, which is why the
  Post/Redirect/Get pattern works without the message re-appearing on refresh.

  data-autohide lets js/app.js fade the box out and pop a toast.
  ============================================================================
-->
<html xmlns:th="http://www.thymeleaf.org">
<body>

<div th:fragment="alerts">

    <!-- Success -->
    <div th:if="${successMessage}" class="alert alert-success" data-autohide="success">
        <i class="bi bi-check-circle-fill"></i>
        <span th:text="${successMessage}">Operation completed.</span>
    </div>

    <!-- Error -->
    <div th:if="${errorMessage}" class="alert alert-danger" data-autohide="error">
        <i class="bi bi-exclamation-octagon-fill"></i>
        <span th:text="${errorMessage}">Something went wrong.</span>
    </div>

    <!-- Information -->
    <div th:if="${infoMessage}" class="alert alert-info" data-autohide="info">
        <i class="bi bi-info-circle-fill"></i>
        <span th:text="${infoMessage}">Please note.</span>
    </div>

    <!-- Logout confirmation, added by Spring Security's logoutSuccessUrl -->
    <div th:if="${param.logout}" class="alert alert-info" data-autohide="info">
        <i class="bi bi-box-arrow-right"></i>
        <span>You have been logged out successfully.</span>
    </div>
</div>

</body>
</html>

```

---

## `portfolio-app/src/main/resources/templates/fragments/footer.html`
<a id="portfolio-app-src-main-resources-templates-fragments-footerhtml"></a>

```html
<!DOCTYPE html>
<!--
  ============================================================================
  FRAGMENT : footer
  ============================================================================
  Usage:  <footer th:replace="~{fragments/footer :: footer}"></footer>

  All links and social URLs come from the site_settings table, so the footer
  updates when the admin edits Settings - no template change needed.
  th:if guards mean a social button disappears when its URL is left empty.
  ============================================================================
-->
<html xmlns:th="http://www.thymeleaf.org">
<body>

<footer th:fragment="footer" class="site-footer">
    <div class="container-px">
        <div class="footer-grid">

            <!-- Column 1 : short intro -->
            <div>
                <a th:href="@{${basePrefix != null ? basePrefix : '/'}}" class="brand mb-2">
                    <span class="brand-mark"><i class="bi bi-braces"></i></span>
                    <span th:text="${settings['hero.name']} ?: 'Vaishnavi Sunil Mali'">Vaishnavi Sunil Mali</span>
                </a>
                <p style="max-width: 380px; font-size: .92rem;"
                   th:text="${settings['hero.title']} ?: 'EXTC Engineering Student & Developer'">
                    EXTC Engineering Student & Developer
                </p>

                <div class="social-row">
                    <a th:if="${settings['social.github']}"
                       th:href="${settings['social.github']}" target="_blank" rel="noopener"
                       class="social-link" title="GitHub">
                        <i class="bi bi-github"></i>
                    </a>
                    <a th:if="${settings['social.linkedin']}"
                       th:href="${settings['social.linkedin']}" target="_blank" rel="noopener"
                       class="social-link" title="LinkedIn">
                        <i class="bi bi-linkedin"></i>
                    </a>
                    <a th:if="${settings['social.twitter']}"
                       th:href="${settings['social.twitter']}" target="_blank" rel="noopener"
                       class="social-link" title="Twitter / X">
                        <i class="bi bi-twitter-x"></i>
                    </a>
                    <a th:if="${settings['social.instagram']}"
                       th:href="${settings['social.instagram']}" target="_blank" rel="noopener"
                       class="social-link" title="Instagram">
                        <i class="bi bi-instagram"></i>
                    </a>
                    <a th:if="${settings['about.email']}"
                       th:href="'mailto:' + ${settings['about.email']}"
                       class="social-link" title="Email">
                        <i class="bi bi-envelope-fill"></i>
                    </a>
                </div>
            </div>

            <!-- Column 2 : quick links -->
            <div>
                <div class="footer-title">Quick Links</div>
                <ul class="footer-links">
                    <li><a th:href="@{${basePrefix != null ? basePrefix : ''} + '/'}">Home</a></li>
                    <li><a th:href="@{${basePrefix != null ? basePrefix : ''} + '/about'}">About Me</a></li>
                    <li><a th:href="@{${basePrefix != null ? basePrefix : ''} + '/projects'}">Projects</a></li>
                    <li><a th:href="@{${basePrefix != null ? basePrefix : ''} + '/skills'}">Skills</a></li>
                    <li><a th:href="@{${basePrefix != null ? basePrefix : ''} + '/contact'}">Contact</a></li>
                </ul>
            </div>

            <!-- Column 3 : profile -->
            <div>
                <div class="footer-title">Portfolio</div>
                <ul class="footer-links">
                    <li><a th:href="@{${basePrefix != null ? basePrefix : ''} + '/education'}">Education</a></li>
                    <li><a th:href="@{${basePrefix != null ? basePrefix : ''} + '/experience'}">Experience</a></li>
                    <li><a th:href="@{${basePrefix != null ? basePrefix : ''} + '/certifications'}">Certifications</a></li>
                    <li><a th:href="@{${basePrefix != null ? basePrefix : ''} + '/achievements'}">Achievements</a></li>
                    <li><a th:href="@{${basePrefix != null ? basePrefix : ''} + '/resume'}">Download Resume</a></li>
                    <li><a th:href="@{/login}">Admin Login</a></li>
                </ul>
            </div>
        </div>

        <div class="footer-bottom">
            <span>
                &copy; <span th:text="${currentYear}">2026</span>
                <span th:text="${settings['hero.name']} ?: 'Vaishnavi Sunil Mali'">Vaishnavi Sunil Mali</span>.
                All rights reserved.
            </span>
            <span>Built with Spring Boot, Thymeleaf &amp; MySQL</span>
        </div>
    </div>
</footer>

</body>
</html>

```

---

## `portfolio-app/src/main/resources/templates/fragments/head.html`
<a id="portfolio-app-src-main-resources-templates-fragments-headhtml"></a>

```html
<!DOCTYPE html>
<!--
  ============================================================================
  FRAGMENT : head
  ============================================================================
  Reusable <head> block. Every public page starts with:

      <head th:replace="~{fragments/head :: head('Page Title')}"></head>

  WHAT IS LOADED
    1. Bootstrap 5 CSS      (CDN) - components, grid, utilities
    2. Bootstrap Icons      (CDN) - the icon font used for small icons
    3. css/style.css        (ours) - loaded LAST so the portfolio design wins

  Because style.css defines its own layout, colours and components, the site
  still looks correct if the CDN cannot be reached (for example when the
  project is demonstrated without an internet connection).
  ============================================================================
-->
<html xmlns:th="http://www.thymeleaf.org">
<head th:fragment="head(pageTitle)">
    <meta charset="UTF-8"/>
    <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
    <meta name="description"
          th:content="${settings['hero.name']} + ' - ' + ${settings['hero.title']}"/>

    <title th:text="${pageTitle} + ' | ' + ${settings['hero.name']}">Portfolio</title>

    <!-- Bootstrap 5 CSS -->
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css"
          rel="stylesheet"
          integrity="sha384-QWTKZyjpPEjISv5WaRU9OFeRpok6YctnYmDr5pNlyT2bRjXh0JMhjY6hW+ALEwIH"
          crossorigin="anonymous"/>

    <!-- Bootstrap Icons -->
    <link href="https://cdn.jsdelivr.net/npm/bootstrap-icons@1.11.3/font/bootstrap-icons.min.css"
          rel="stylesheet"/>

    <!-- Our stylesheet - must come after Bootstrap -->
    <link rel="stylesheet" th:href="@{/css/style.css}"/>
    <link rel="stylesheet" th:href="@{/css/admin.css}"/>

    <!-- Favicon (inline SVG data URI, so no extra file is needed) -->
    <link rel="icon"
          href="data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 32 32'%3E%3Crect width='32' height='32' rx='8' fill='%234f7cff'/%3E%3Ctext x='16' y='22' font-size='16' font-family='Arial' font-weight='bold' fill='white' text-anchor='middle'%3EP%3C/text%3E%3C/svg%3E"/>

    <!-- Small script in the head prevents a white flash before the theme loads -->
    <script th:inline="javascript">
        (function () {
            var saved = localStorage.getItem('portfolio-theme');
            if (saved === 'light' || saved === 'dark') {
                document.documentElement.setAttribute('data-theme', saved);
            }
        })();
    </script>
</head>
<body>
</body>
</html>

```

---

## `portfolio-app/src/main/resources/templates/fragments/navbar.html`
<a id="portfolio-app-src-main-resources-templates-fragments-navbarhtml"></a>

```html
<!DOCTYPE html>
<!--
  ============================================================================
  FRAGMENT : navbar  (sticky navigation for the public website)
  ============================================================================
  Usage:  <nav th:replace="~{fragments/navbar :: navbar}"></nav>

  The controller puts an "activeSection" attribute in the model; each link
  compares itself against that value to add the .active class.

  On screens narrower than 992px the link list collapses and the hamburger
  button toggles the .open class (see js/app.js).
  ============================================================================
-->
<html xmlns:th="http://www.thymeleaf.org">
<body>

<nav th:fragment="navbar" class="site-navbar" id="siteNavbar">
    <div class="navbar-inner">

        <!-- Brand -->
        <a th:href="@{${basePrefix != null ? basePrefix : '/'}}" class="brand">
            <span class="brand-mark">
                <i class="bi bi-braces"></i>
            </span>
            <span th:text="${settings['hero.name']} ?: 'Vaishnavi Sunil Mali'">Vaishnavi Sunil Mali</span>
        </a>

        <!-- Links (collapses into the hamburger menu on mobile) -->
        <ul class="nav-links" id="navLinks">
            <li><a th:href="@{${basePrefix != null ? basePrefix : ''} + '/'}"
                   th:classappend="${activeSection == 'home'} ? 'active'">Home</a></li>
            <li><a th:href="@{${basePrefix != null ? basePrefix : ''} + '/about'}"
                   th:classappend="${activeSection == 'about'} ? 'active'">About</a></li>
            <li><a th:href="@{${basePrefix != null ? basePrefix : ''} + '/skills'}"
                   th:classappend="${activeSection == 'skills'} ? 'active'">Skills</a></li>
            <li><a th:href="@{${basePrefix != null ? basePrefix : ''} + '/projects'}"
                   th:classappend="${activeSection == 'projects'} ? 'active'">Projects</a></li>
            <li><a th:href="@{${basePrefix != null ? basePrefix : ''} + '/education'}"
                   th:classappend="${activeSection == 'education'} ? 'active'">Education</a></li>
            <li><a th:href="@{${basePrefix != null ? basePrefix : ''} + '/experience'}"
                   th:classappend="${activeSection == 'experience'} ? 'active'">Experience</a></li>
            <li><a th:href="@{${basePrefix != null ? basePrefix : ''} + '/certifications'}"
                   th:classappend="${activeSection == 'certifications'} ? 'active'">Certificates</a></li>
            <li><a th:href="@{${basePrefix != null ? basePrefix : ''} + '/achievements'}"
                   th:classappend="${activeSection == 'achievements'} ? 'active'">Achievements</a></li>
            <li><a th:href="@{${basePrefix != null ? basePrefix : ''} + '/contact'}"
                   th:classappend="${activeSection == 'contact'} ? 'active'">Contact</a></li>
            <li><a th:href="@{/explore}"
                   th:classappend="${activeSection == 'explore'} ? 'active'">
                <i class="bi bi-compass me-1"></i>Explore
            </a></li>
        </ul>

        <!-- Right side actions -->
        <div class="navbar-actions">
            <!-- Authenticated User Menu -->
            <div th:if="${currentUser != null}" class="d-inline-flex align-items-center gap-2">
                <a th:href="@{/admin/dashboard}" class="btn btn-outline-primary btn-sm d-none d-sm-inline-flex align-items-center gap-1"
                   title="Go to Dashboard">
                    <i class="bi bi-speedometer2"></i>
                    <span th:text="${currentUser.username}">Dashboard</span>
                </a>
                <form th:action="@{/logout}" method="post" class="d-inline m-0">
                    <button type="submit" class="icon-btn text-danger" title="Sign Out" aria-label="Sign Out">
                        <i class="bi bi-box-arrow-right"></i>
                    </button>
                </form>
            </div>

            <!-- Anonymous / Guest buttons -->
            <div th:if="${currentUser == null}" class="d-inline-flex align-items-center gap-2">
                <a th:href="@{/login}" class="btn btn-outline-primary btn-sm d-inline-flex align-items-center gap-1">
                    <i class="bi bi-box-arrow-in-right"></i>
                    <span>Sign In</span>
                </a>
                <a th:href="@{/register}" class="btn btn-primary btn-sm d-none d-sm-inline-flex align-items-center gap-1">
                    <i class="bi bi-person-plus"></i>
                    <span>Sign Up</span>
                </a>
            </div>

            <!-- Dark / light theme toggle -->
            <button type="button" class="icon-btn" id="themeToggle"
                    title="Toggle dark / light mode" aria-label="Toggle theme">
                <i class="bi bi-moon-stars-fill" id="themeIcon"></i>
            </button>

            <!-- Hamburger (mobile only) -->
            <button type="button" class="navbar-toggle" id="navbarToggle"
                    aria-label="Open menu" aria-expanded="false" aria-controls="navLinks">
                <i class="bi bi-list"></i>
            </button>
        </div>
    </div>
</nav>

</body>
</html>

```

---

## `portfolio-app/src/main/resources/templates/fragments/scripts.html`
<a id="portfolio-app-src-main-resources-templates-fragments-scriptshtml"></a>

```html
<!DOCTYPE html>
<!--
  ============================================================================
  FRAGMENT : scripts
  ============================================================================
  Usage:  <div th:replace="~{fragments/scripts :: scripts}"></div>
          just before </body>

  Loads Bootstrap's JavaScript bundle (used for the mobile nav behaviour and
  any Bootstrap component) followed by our own js/app.js.
  ============================================================================
-->
<html xmlns:th="http://www.thymeleaf.org">
<body>

<div th:fragment="scripts">
    <!-- Bootstrap 5 bundle (Popper included) -->
    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/js/bootstrap.bundle.min.js"
            integrity="sha384-YvpcrYf0tY3lHB60NNkmXc5s9fDVZLESaAA55NDzOxhy9GkcIdslK1eN7N6jIeHz"
            crossorigin="anonymous"></script>

    <!-- Our JavaScript: theme toggle, nav, animations, filtering, validation -->
    <script th:src="@{/js/app.js}"></script>
</div>

</body>
</html>

```

---

# 12. Public Website Templates

## `portfolio-app/src/main/resources/templates/public/about.html`
<a id="portfolio-app-src-main-resources-templates-public-abouthtml"></a>

```html
<!DOCTYPE html>
<!--
  ============================================================================
  TEMPLATE : public/about.html   ->  GET /about
  ============================================================================
  Profile picture, introduction, career objective, interests, personal
  information and the live statistics.
  ============================================================================
-->
<html lang="en" xmlns:th="http://www.thymeleaf.org">
<head th:replace="~{fragments/head :: head('About Me')}"></head>
<body>

<div class="bg-glow"></div>
<nav th:replace="~{fragments/navbar :: navbar}"></nav>

<main>
    <header class="page-header">
        <div class="container-px">
            <div class="breadcrumb-line">
                <a th:href="@{${basePrefix != null ? basePrefix : '/'}}">Home</a> <span>/</span> <span>About</span>
            </div>
            <h1>About Me</h1>
            <p>A little background on who I am, what I am learning and where I am heading.</p>
        </div>
    </header>

    <section class="section">
        <div class="container-px">
            <div class="about-grid">

                <!-- Left : photo -->
                <div class="text-center reveal">
                    <img class="about-avatar"
                         th:src="${settings['profile.image']} ?: @{/img/profile-placeholder.svg}"
                         alt="Profile photo"/>
                    <div class="mt-2 gap-row" style="justify-content:center;">
                        <a th:href="@{${basePrefix != null ? basePrefix : ''} + '/resume'}" class="btn btn-primary btn-sm">
                            <i class="bi bi-download"></i> Resume
                        </a>
                        <a th:href="@{${basePrefix != null ? basePrefix : ''} + '/contact'}" class="btn btn-outline btn-sm">
                            <i class="bi bi-chat-dots"></i> Hire Me
                        </a>
                    </div>
                </div>

                <!-- Right : text -->
                <div class="reveal reveal-delay-1">
                    <span class="eyebrow"
                          style="background:var(--gradient);-webkit-background-clip:text;background-clip:text;color:transparent;font-weight:700;letter-spacing:.14em;text-transform:uppercase;font-size:.78rem;">
                        Introduction
                    </span>
                    <h2 th:text="${settings['hero.name']} ?: 'Vaishnavi Sunil Mali'">Vaishnavi Sunil Mali</h2>
                    <p th:text="${settings['about.intro']}">Introduction paragraph.</p>

                    <h3 class="mt-2">Career Objective</h3>
                    <p th:text="${settings['about.objective']}">Career objective.</p>

                    <!-- Interests -->
                    <h3 class="mt-2">Interests</h3>
                    <div class="chip-row mb-2">
                        <span class="badge badge-soft" th:each="interest : ${interests}"
                              th:text="${interest}">Interest</span>
                        <span th:if="${#lists.isEmpty(interests)}" class="text-muted">
                            Add interests from the admin panel.
                        </span>
                    </div>

                    <!-- Languages -->
                    <th:block th:unless="${#lists.isEmpty(languages)}">
                        <h3 class="mt-2">Languages</h3>
                        <div class="chip-row mb-2">
                            <span class="badge" th:each="language : ${languages}"
                                  th:text="${language}">Language</span>
                        </div>
                    </th:block>
                </div>
            </div>
        </div>
    </section>

    <!-- Personal information -->
    <section class="section section-alt section-tight">
        <div class="container-px">
            <div class="section-heading reveal">
                <span class="eyebrow">Details</span>
                <h2>Personal Information</h2>
            </div>

            <div class="card-glass reveal">
                <ul class="info-list">
                    <li>
                        <span class="info-key">Full Name</span>
                        <span class="info-val" th:text="${settings['hero.name']} ?: 'Vaishnavi Sunil Mali'">Vaishnavi Sunil Mali</span>
                    </li>
                    <li th:if="${settings['about.dob'] != null and !settings['about.dob'].isBlank()}">
                        <span class="info-key">Date of Birth</span>
                        <span class="info-val" th:text="${settings['about.dob']}">-</span>
                    </li>
                    <li>
                        <span class="info-key">Email</span>
                        <span class="info-val" th:text="${settings['about.email']} ?: 'vaishnavim25extc@student.mes.ac.in'">vaishnavim25extc@student.mes.ac.in</span>
                    </li>
                    <li th:if="${settings['about.phone'] != null and !settings['about.phone'].isBlank()}">
                        <span class="info-key">Phone</span>
                        <span class="info-val" th:text="${settings['about.phone']}">-</span>
                    </li>
                    <li>
                        <span class="info-key">Location</span>
                        <span class="info-val" th:text="${settings['about.location']} ?: 'Kharghar, Mumbai, Maharashtra, India'">Kharghar, Mumbai, Maharashtra, India</span>
                    </li>
                    <li>
                        <span class="info-key">Current Title</span>
                        <span class="info-val" th:text="${settings['hero.title']} ?: 'EXTC Engineering Student & Developer'">EXTC Engineering Student & Developer</span>
                    </li>
                </ul>
            </div>
        </div>
    </section>

    <!-- Statistics -->
    <section class="section">
        <div class="container-px">
            <div class="section-heading reveal">
                <span class="eyebrow">By The Numbers</span>
                <h2>Statistics</h2>
                <p>These numbers are counted live from the database, so they update automatically
                   whenever something is added in the admin panel.</p>
            </div>

            <div class="row-grid">
                <div class="col col-4 reveal">
                    <div class="card-glass stat-card">
                        <div class="stat-value" th:text="${stats['projects']}">0</div>
                        <div class="stat-label">Projects Completed</div>
                    </div>
                </div>
                <div class="col col-4 reveal reveal-delay-1">
                    <div class="card-glass stat-card">
                        <div class="stat-value" th:text="${stats['certifications']}">0</div>
                        <div class="stat-label">Certifications</div>
                    </div>
                </div>
                <div class="col col-4 reveal reveal-delay-2">
                    <div class="card-glass stat-card">
                        <div class="stat-value" th:text="${stats['skills']}">0</div>
                        <div class="stat-label">Technologies</div>
                    </div>
                </div>
                <div class="col col-4 reveal">
                    <div class="card-glass stat-card">
                        <div class="stat-value" th:text="${stats['hackathons']}">0</div>
                        <div class="stat-label">Hackathons</div>
                    </div>
                </div>
                <div class="col col-4 reveal reveal-delay-1">
                    <div class="card-glass stat-card">
                        <div class="stat-value" th:text="${stats['achievements']}">0</div>
                        <div class="stat-label">Achievements</div>
                    </div>
                </div>
                <div class="col col-4 reveal reveal-delay-2">
                    <div class="card-glass stat-card">
                        <div class="stat-value" th:text="${stats['experiences']}">0</div>
                        <div class="stat-label">Work Experiences</div>
                    </div>
                </div>
            </div>
        </div>
    </section>
</main>

<footer th:replace="~{fragments/footer :: footer}"></footer>
<button id="backToTop" title="Back to top"><i class="bi bi-arrow-up"></i></button>
<div id="toastContainer"></div>
<div th:replace="~{fragments/scripts :: scripts}"></div>
</body>
</html>

```

---

## `portfolio-app/src/main/resources/templates/public/achievements.html`
<a id="portfolio-app-src-main-resources-templates-public-achievementshtml"></a>

```html
<!DOCTYPE html>
<!--
  ============================================================================
  TEMPLATE : public/achievements.html   ->  GET /achievements
  ============================================================================
  The badge colour comes from Achievement.getBadgeClass(), so the view stays
  free of if/else logic about categories.
  ============================================================================
-->
<html lang="en" xmlns:th="http://www.thymeleaf.org">
<head th:replace="~{fragments/head :: head('Achievements')}"></head>
<body>

<div class="bg-glow"></div>
<nav th:replace="~{fragments/navbar :: navbar}"></nav>

<main>
    <header class="page-header">
        <div class="container-px">
            <div class="breadcrumb-line">
                <a th:href="@{${basePrefix != null ? basePrefix : '/'}}">Home</a> <span>/</span> <span>Achievements</span>
            </div>
            <h1>Achievements</h1>
            <p>Hackathons, competitions, awards and academic milestones.</p>
        </div>
    </header>

    <section class="section">
        <div class="container-px">

            <div th:if="${#lists.isEmpty(achievements)}" class="empty-state reveal">
                <div class="empty-icon"><i class="bi bi-trophy"></i></div>
                <h3 style="margin-bottom:8px;">No achievements added yet.</h3>
                <p class="text-muted" style="max-width:500px; margin:0 auto;">
                    Academic milestones, project competitions, and technical awards will appear here once added.
                </p>
            </div>

            <div class="row-grid" th:unless="${#lists.isEmpty(achievements)}">
                <div class="col col-4 reveal" th:each="ach, iter : ${achievements}"
                     th:classappend="' reveal-delay-' + ${(iter.index % 3) + 1}">
                    <div class="card-glass">
                        <div class="spread mb-2">
                            <span class="badge" th:classappend="${ach.badgeClass}"
                                  th:text="${ach.category}">Achievement</span>
                            <span class="text-muted" style="font-size:.8rem;"
                                  th:if="${ach.achievementDate}"
                                  th:text="${#temporals.format(ach.achievementDate, 'MMM yyyy')}">
                                Jan 2026
                            </span>
                        </div>

                        <h3 class="card-title" th:text="${ach.title}">Achievement Title</h3>
                        <p class="card-text" th:text="${ach.description}">Description.</p>

                        <div class="spread" style="margin-top:auto;">
                            <span class="text-muted" style="font-size:.85rem;"
                                  th:if="${ach.organization}">
                                <i class="bi bi-award"></i>
                                <span th:text="${ach.organization}">Organization</span>
                            </span>
                            <a th:if="${ach.linkUrl}" th:href="${ach.linkUrl}"
                               target="_blank" rel="noopener" class="btn btn-outline btn-sm">
                                <i class="bi bi-box-arrow-up-right"></i> Details
                            </a>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>
</main>

<footer th:replace="~{fragments/footer :: footer}"></footer>
<button id="backToTop" title="Back to top"><i class="bi bi-arrow-up"></i></button>
<div id="toastContainer"></div>
<div th:replace="~{fragments/scripts :: scripts}"></div>
</body>
</html>

```

---

## `portfolio-app/src/main/resources/templates/public/certifications.html`
<a id="portfolio-app-src-main-resources-templates-public-certificationshtml"></a>

```html
<!DOCTYPE html>
<!--
  ============================================================================
  TEMPLATE : public/certifications.html   ->  GET /certifications
  ============================================================================
  ============================================================================
-->
<html lang="en" xmlns:th="http://www.thymeleaf.org">
<head th:replace="~{fragments/head :: head('Certifications')}"></head>
<body>

<div class="bg-glow"></div>
<nav th:replace="~{fragments/navbar :: navbar}"></nav>

<main>
    <header class="page-header">
        <div class="container-px">
            <div class="breadcrumb-line">
                <a th:href="@{${basePrefix != null ? basePrefix : '/'}}">Home</a> <span>/</span> <span>Certifications</span>
            </div>
            <h1>Certifications</h1>
            <p>
                <span th:text="${#lists.size(certifications)}">0</span> courses and
                certifications I have completed.
            </p>
        </div>
    </header>

    <section class="section">
        <div class="container-px">

            <div th:if="${#lists.isEmpty(certifications)}" class="empty-state reveal">
                <div class="empty-icon"><i class="bi bi-patch-check"></i></div>
                <h3 style="margin-bottom:8px;">No certifications added yet.</h3>
                <p class="text-muted" style="max-width:500px; margin:0 auto;">
                    Professional technical certifications and completed coursework will be listed here.
                </p>
            </div>

            <div class="row-grid" th:unless="${#lists.isEmpty(certifications)}">
                <div class="col col-4 reveal" th:each="cert, iter : ${certifications}"
                     th:classappend="' reveal-delay-' + ${(iter.index % 3) + 1}">
                    <div class="card-glass">
                        <div class="cert-thumb">
                            <img th:src="${cert.imageUrl} ?: @{/img/certificate-placeholder.svg}"
                                 th:alt="${cert.title}" loading="lazy"/>
                        </div>

                        <h3 class="card-title" th:text="${cert.title}">Certificate Title</h3>
                        <p class="card-text">
                            <i class="bi bi-building"></i>
                            <span th:text="${cert.issuer}">Issuer</span>
                        </p>

                        <div class="chip-row mb-2">
                            <span class="badge" th:if="${cert.issueDate}"
                                  th:text="${#temporals.format(cert.issueDate, 'MMM yyyy')}">Jan 2026</span>
                            <span class="badge badge-soft" th:if="${cert.credentialId}"
                                  th:text="'ID: ' + ${cert.credentialId}">ID: 0001</span>
                        </div>

                        <div class="project-actions">
                            <a th:if="${cert.certificateUrl}" th:href="${cert.certificateUrl}"
                               target="_blank" rel="noopener" class="btn btn-primary btn-sm">
                                <i class="bi bi-file-earmark-check"></i> View Certificate
                            </a>
                            <span th:unless="${cert.certificateUrl}" class="text-muted"
                                  style="font-size:.85rem;">No certificate link added.</span>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>
</main>

<footer th:replace="~{fragments/footer :: footer}"></footer>
<button id="backToTop" title="Back to top"><i class="bi bi-arrow-up"></i></button>
<div id="toastContainer"></div>
<div th:replace="~{fragments/scripts :: scripts}"></div>
</body>
</html>

```

---

## `portfolio-app/src/main/resources/templates/public/contact.html`
<a id="portfolio-app-src-main-resources-templates-public-contacthtml"></a>

```html
<!DOCTYPE html>
<!--
  ============================================================================
  TEMPLATE : public/contact.html   ->  GET /contact
  ============================================================================
  THE FORM HAS TWO SUBMISSION PATHS
    1. With JavaScript (normal case)
       app.js intercepts the submit, validates the fields in the browser and
       POSTs to /contact/submit-ajax with fetch(). A toast confirms the result
       and the page never reloads.

    2. Without JavaScript
       The form's own action is /contact/submit, so a plain POST still stores
       the message and comes back with a flash message. Nothing breaks.

  th:object + th:field binds the form to the ContactMessage model attribute,
  and th:errors prints the Bean Validation messages when the server rejects
  the submission.
  ============================================================================
-->
<html lang="en" xmlns:th="http://www.thymeleaf.org">
<head th:replace="~{fragments/head :: head('Contact')}"></head>
<body>

<div class="bg-glow"></div>
<nav th:replace="~{fragments/navbar :: navbar}"></nav>

<main>
    <header class="page-header">
        <div class="container-px">
            <div class="breadcrumb-line">
                <a th:href="@{${basePrefix != null ? basePrefix : '/'}}">Home</a> <span>/</span> <span>Contact</span>
            </div>
            <h1>Get In Touch</h1>
            <p>Send me a message and I will reply as soon as I can.</p>
        </div>
    </header>

    <section class="section">
        <div class="container-px">
            <div class="row-grid">

                <!-- LEFT : contact details -->
                <div class="col col-4 reveal">
                    <div class="card-glass">
                        <h3 class="card-title">Contact Information</h3>
                        <p class="card-text">
                            Feel free to reach out for internships, freelance work or
                            just to talk about Java and Spring Boot.
                        </p>

                        <ul class="bullet-list">
                            <li th:if="${settings['about.email']}">
                                <strong>Email:</strong>
                                <span th:text="${settings['about.email']}">email@example.com</span>
                            </li>
                            <li th:if="${settings['about.phone']}">
                                <strong>Phone:</strong>
                                <span th:text="${settings['about.phone']}">+91 ...</span>
                            </li>
                            <li th:if="${settings['about.location']}">
                                <strong>Location:</strong>
                                <span th:text="${settings['about.location']}">City, India</span>
                            </li>
                        </ul>

                        <div class="divider"></div>

                        <div class="footer-title">Follow Me</div>
                        <div class="social-row">
                            <a th:if="${settings['social.github']}"
                               th:href="${settings['social.github']}" target="_blank" rel="noopener"
                               class="social-link" title="GitHub"><i class="bi bi-github"></i></a>
                            <a th:if="${settings['social.linkedin']}"
                               th:href="${settings['social.linkedin']}" target="_blank" rel="noopener"
                               class="social-link" title="LinkedIn"><i class="bi bi-linkedin"></i></a>
                            <a th:if="${settings['social.twitter']}"
                               th:href="${settings['social.twitter']}" target="_blank" rel="noopener"
                               class="social-link" title="Twitter"><i class="bi bi-twitter-x"></i></a>
                            <a th:if="${settings['social.instagram']}"
                               th:href="${settings['social.instagram']}" target="_blank" rel="noopener"
                               class="social-link" title="Instagram"><i class="bi bi-instagram"></i></a>
                        </div>
                    </div>
                </div>

                <!-- RIGHT : the form -->
                <div class="col" style="flex:0 0 66.6666%; max-width:66.6666%;" >
                    <div class="card-glass reveal reveal-delay-1">
                        <h3 class="card-title">Send a Message</h3>
                        <p class="card-text">
                            All fields marked <span style="color:#ff6b78;">*</span> are required.
                        </p>

                        <!-- Server side flash messages (no-JavaScript path) -->
                        <div th:replace="~{fragments/alerts :: alerts}"></div>

                        <form id="contactForm"
                              th:action="@{${contactAction ?: '/contact/submit'}}"
                              th:attr="data-action=@{${contactAjaxAction ?: '/contact/submit-ajax'}}"
                              th:object="${contactMessage}"
                              method="post"
                              novalidate>

                            <div class="form-row">
                                <div class="form-group">
                                    <label class="form-label" for="name">
                                        Your Name <span class="req">*</span>
                                    </label>
                                    <input type="text" class="form-control" id="name"
                                           th:field="*{name}" placeholder="John Doe"
                                           minlength="2" maxlength="80" required/>
                                    <div class="invalid-feedback"
                                         th:if="${#fields.hasErrors('name')}"
                                         th:errors="*{name}">Name error</div>
                                </div>

                                <div class="form-group">
                                    <label class="form-label" for="email">
                                        Email Address <span class="req">*</span>
                                    </label>
                                    <input type="email" class="form-control" id="email"
                                           th:field="*{email}" placeholder="john@example.com"
                                           maxlength="120" required/>
                                    <div class="invalid-feedback"
                                         th:if="${#fields.hasErrors('email')}"
                                         th:errors="*{email}">Email error</div>
                                </div>
                            </div>

                            <div class="form-group">
                                <label class="form-label" for="subject">
                                    Subject <span class="req">*</span>
                                </label>
                                <input type="text" class="form-control" id="subject"
                                       th:field="*{subject}" placeholder="Internship opportunity"
                                       minlength="3" maxlength="150" required/>
                                <div class="invalid-feedback"
                                     th:if="${#fields.hasErrors('subject')}"
                                     th:errors="*{subject}">Subject error</div>
                            </div>

                            <div class="form-group">
                                <label class="form-label" for="message">
                                    Message <span class="req">*</span>
                                </label>
                                <textarea class="form-control" id="message"
                                          th:field="*{message}"
                                          data-maxlength="2000"
                                          placeholder="Write your message here (at least 10 characters)..."
                                          minlength="10" maxlength="2000" required></textarea>
                                <div class="invalid-feedback"
                                     th:if="${#fields.hasErrors('message')}"
                                     th:errors="*{message}">Message error</div>
                            </div>

                            <button type="submit" class="btn btn-primary btn-lg btn-block">
                                <i class="bi bi-send-fill"></i> Send Message
                            </button>
                        </form>
                    </div>
                </div>
            </div>
        </div>
    </section>
</main>

<footer th:replace="~{fragments/footer :: footer}"></footer>
<button id="backToTop" title="Back to top"><i class="bi bi-arrow-up"></i></button>
<div id="toastContainer"></div>
<div th:replace="~{fragments/scripts :: scripts}"></div>
</body>
</html>

```

---

## `portfolio-app/src/main/resources/templates/public/education.html`
<a id="portfolio-app-src-main-resources-templates-public-educationhtml"></a>

```html
<!DOCTYPE html>
<!--
  ============================================================================
  TEMPLATE : public/education.html   ->  GET /education
  ============================================================================
  Vertical timeline built from the educations table, newest qualification first.
  ============================================================================
-->
<html lang="en" xmlns:th="http://www.thymeleaf.org">
<head th:replace="~{fragments/head :: head('Education')}"></head>
<body>

<div class="bg-glow"></div>
<nav th:replace="~{fragments/navbar :: navbar}"></nav>

<main>
    <header class="page-header">
        <div class="container-px">
            <div class="breadcrumb-line">
                <a th:href="@{${basePrefix != null ? basePrefix : '/'}}">Home</a> <span>/</span> <span>Education</span>
            </div>
            <h1>Education</h1>
            <p>My academic background, newest qualification first.</p>
        </div>
    </header>

    <section class="section">
        <div class="container-px">

            <div th:if="${#lists.isEmpty(educations)}" class="empty-state reveal">
                <div class="empty-icon"><i class="bi bi-mortarboard"></i></div>
                <p>No education entries yet. Add them from the admin panel.</p>
            </div>

            <div class="timeline" th:unless="${#lists.isEmpty(educations)}">
                <div class="timeline-item reveal" th:each="edu : ${educations}">
                    <span class="timeline-dot"></span>

                    <div class="timeline-date" th:text="${edu.yearRange}">2022 - 2026</div>

                    <div class="timeline-card">
                        <div class="spread">
                            <h3 th:text="${edu.degree}">Degree</h3>
                            <span class="badge badge-gradient"
                                  th:if="${edu.percentageOrCgpa}"
                                  th:text="${edu.percentageOrCgpa}">8.70 CGPA</span>
                        </div>

                        <div class="timeline-sub">
                            <i class="bi bi-building"></i>
                            <span th:text="${edu.institution}">Institution</span>
                        </div>

                        <p th:if="${edu.description}" th:text="${edu.description}"
                           style="margin:0; font-size:.93rem;">
                            Description.
                        </p>
                    </div>
                </div>
            </div>

            <div class="text-center mt-3">
                <a th:href="@{${basePrefix != null ? basePrefix : ''} + '/experience'}" class="btn btn-outline">
                    See my work experience <i class="bi bi-arrow-right"></i>
                </a>
            </div>
        </div>
    </section>
</main>

<footer th:replace="~{fragments/footer :: footer}"></footer>
<button id="backToTop" title="Back to top"><i class="bi bi-arrow-up"></i></button>
<div id="toastContainer"></div>
<div th:replace="~{fragments/scripts :: scripts}"></div>
</body>
</html>

```

---

## `portfolio-app/src/main/resources/templates/public/experience.html`
<a id="portfolio-app-src-main-resources-templates-public-experiencehtml"></a>

```html
<!DOCTYPE html>
<!--
  ============================================================================
  TEMPLATE : public/experience.html   ->  GET /experience
  ============================================================================
  Professional timeline. The entity's getDateRange() returns
  "Jun 2025 - Present" when endDate is null.
  ============================================================================
-->
<html lang="en" xmlns:th="http://www.thymeleaf.org">
<head th:replace="~{fragments/head :: head('Experience')}"></head>
<body>

<div class="bg-glow"></div>
<nav th:replace="~{fragments/navbar :: navbar}"></nav>

<main>
    <header class="page-header">
        <div class="container-px">
            <div class="breadcrumb-line">
                <a th:href="@{${basePrefix != null ? basePrefix : '/'}}">Home</a> <span>/</span> <span>Experience</span>
            </div>
            <h1>Work Experience</h1>
            <p>Internships, jobs and roles where I applied what I learned.</p>
        </div>
    </header>

    <section class="section">
        <div class="container-px">

            <div th:if="${#lists.isEmpty(experiences)}" class="empty-state reveal">
                <div class="empty-icon"><i class="bi bi-briefcase"></i></div>
                <h3 style="margin-bottom:8px;">Experience details will be added soon.</h3>
                <p class="text-muted" style="max-width:500px; margin:0 auto 16px;">
                    Currently focused on academics, coursework, and technical projects. Work experience, internships, and research training will be listed here.
                </p>
                <a th:href="@{${basePrefix != null ? basePrefix : ''} + '/projects'}" class="btn btn-outline btn-sm">
                    <i class="bi bi-collection me-1"></i> Browse Projects
                </a>
            </div>

            <div class="timeline" th:unless="${#lists.isEmpty(experiences)}">
                <div class="timeline-item reveal" th:each="exp : ${experiences}">
                    <span class="timeline-dot"></span>

                    <div class="timeline-date" th:text="${exp.dateRange}">Jun 2025 - Present</div>

                    <div class="timeline-card">
                        <div class="spread">
                            <h3 th:text="${exp.position}">Position</h3>
                            <span class="badge badge-success" th:if="${exp.endDate == null}">
                                Current
                            </span>
                        </div>

                        <div class="timeline-sub">
                            <i class="bi bi-building"></i>
                            <span th:text="${exp.organization}">Organization</span>
                        </div>

                        <ul class="bullet-list" th:unless="${#lists.isEmpty(exp.responsibilityList)}">
                            <li th:each="item : ${exp.responsibilityList}" th:text="${item}">
                                Responsibility
                            </li>
                        </ul>

                        <div class="chip-row" th:unless="${#lists.isEmpty(exp.technologyList)}">
                            <span class="badge badge-soft"
                                  th:each="tech : ${exp.technologyList}"
                                  th:text="${tech}">Java</span>
                        </div>
                    </div>
                </div>
            </div>

            <div class="text-center mt-3">
                <a th:href="@{${basePrefix != null ? basePrefix : ''} + '/projects'}" class="btn btn-outline">
                    See what I have built <i class="bi bi-arrow-right"></i>
                </a>
            </div>
        </div>
    </section>
</main>

<footer th:replace="~{fragments/footer :: footer}"></footer>
<button id="backToTop" title="Back to top"><i class="bi bi-arrow-up"></i></button>
<div id="toastContainer"></div>
<div th:replace="~{fragments/scripts :: scripts}"></div>
</body>
</html>

```

---

## `portfolio-app/src/main/resources/templates/public/explore.html`
<a id="portfolio-app-src-main-resources-templates-public-explorehtml"></a>

```html
<!DOCTYPE html>
<html lang="en" xmlns:th="http://www.thymeleaf.org">
<head th:replace="~{fragments/head :: head('Explore Developer Portfolios')}"></head>
<body>

<div class="bg-glow"></div>
<nav th:replace="~{fragments/navbar :: navbar}"></nav>

<main class="page-content" style="padding-top: 100px; min-height: 80vh;">
    <div class="container py-4">

        <!-- Header -->
        <div class="text-center mb-5">
            <span class="badge rounded-pill bg-primary bg-opacity-10 text-primary px-3 py-2 mb-2 fw-semibold">
                <i class="bi bi-people-fill me-1"></i> Developer Community
            </span>
            <h1 class="display-5 fw-bold mb-2">Explore Portfolios</h1>
            <p class="text-muted lead mx-auto" style="max-width: 600px;">
                Discover talented software engineers, view their projects, skills, achievements, and get in touch.
            </p>

            <!-- Search bar -->
            <form th:action="@{/explore}" method="get" class="mx-auto mt-4" style="max-width: 540px;">
                <div class="input-group input-group-lg shadow-sm">
                    <span class="input-group-text bg-card border-end-0"><i class="bi bi-search"></i></span>
                    <input type="text" name="keyword" th:value="${keyword}" class="form-control bg-card border-start-0"
                           placeholder="Search by name, headline, email, or skill..."/>
                    <button class="btn btn-primary px-4" type="submit">Search</button>
                    <a th:if="${keyword != null and !keyword.isBlank()}" th:href="@{/explore}"
                       class="btn btn-outline-secondary" title="Clear filter">
                        <i class="bi bi-x-lg"></i>
                    </a>
                </div>
            </form>
        </div>

        <!-- User Cards Grid -->
        <div th:if="${users != null and !users.isEmpty()}" class="row g-4 justify-content-center">
            <div th:each="u : ${users}" class="col-12 col-md-6 col-lg-4">
                <div class="card h-100 card-glass border shadow-sm p-4 d-flex flex-column justify-content-between"
                     style="border-radius: 18px; transition: transform .2s ease, box-shadow .2s ease;">

                    <div>
                        <!-- Avatar & Header -->
                        <div class="d-flex align-items-center gap-3 mb-3">
                            <div class="rounded-circle overflow-hidden d-flex align-items-center justify-content-center"
                                 style="width: 58px; height: 58px; background: var(--gradient); color: #fff; font-size: 1.5rem; flex-shrink: 0;">
                                <img th:if="${u.avatarUrl != null and !u.avatarUrl.isBlank()}"
                                     th:src="@{${u.avatarUrl}}" alt="Avatar"
                                     style="width: 100%; height: 100%; object-fit: cover;"
                                     onerror="this.style.display='none'"/>
                                <span th:text="${u.fullName != null and !u.fullName.isBlank() ? #strings.substring(u.fullName, 0, 1).toUpperCase() : 'U'}">U</span>
                            </div>
                            <div class="overflow-hidden">
                                <h5 class="mb-0 fw-bold text-truncate" th:text="${u.fullName ?: u.username}">Full Name</h5>
                                <div class="text-muted small">@<span th:text="${u.username}">username</span></div>
                            </div>
                        </div>

                        <!-- Headline -->
                        <p class="text-primary small fw-semibold mb-2"
                           th:text="${u.headline ?: 'Software Engineer'}">Software Engineer</p>

                        <!-- Bio snippet -->
                        <p class="text-muted small mb-3" style="min-height: 40px; display: -webkit-box; -webkit-line-clamp: 2; -webkit-box-orient: vertical; overflow: hidden;"
                           th:text="${u.bio ?: 'Passionate about crafting high-performance, robust software solutions.'}">
                            Bio snippet...
                        </p>

                        <!-- Meta Info -->
                        <div class="d-flex flex-wrap gap-2 mb-3">
                            <span th:if="${u.location != null and !u.location.isBlank()}"
                                  class="badge bg-secondary bg-opacity-25 text-secondary">
                                <i class="bi bi-geo-alt me-1"></i><span th:text="${u.location}">Location</span>
                            </span>
                            <span th:if="${u.email != null and !u.email.isBlank()}"
                                  class="badge bg-secondary bg-opacity-25 text-secondary text-truncate" style="max-width: 190px;">
                                <i class="bi bi-envelope me-1"></i><span th:text="${u.email}">email</span>
                            </span>
                        </div>
                    </div>

                    <!-- Actions -->
                    <div class="pt-3 border-top d-flex gap-2">
                        <a th:href="@{'/u/' + ${u.username}}" class="btn btn-primary btn-sm flex-fill">
                            <i class="bi bi-window-fullscreen me-1"></i> View Portfolio
                        </a>
                        <a th:href="@{'/u/' + ${u.username} + '/resume'}" target="_blank"
                           class="btn btn-outline-secondary btn-sm" title="Download PDF Resume">
                            <i class="bi bi-file-earmark-pdf"></i>
                        </a>
                    </div>

                </div>
            </div>
        </div>

        <!-- Empty state -->
        <div th:if="${users == null or users.isEmpty()}" class="text-center py-5">
            <div class="display-1 text-muted mb-3"><i class="bi bi-search"></i></div>
            <h4>No portfolios found</h4>
            <p class="text-muted">No public profiles matched your query "<span th:text="${keyword}">keyword</span>".</p>
            <a th:href="@{/explore}" class="btn btn-primary mt-2">View All Portfolios</a>
        </div>

    </div>
</main>

<footer th:replace="~{fragments/footer :: footer}"></footer>
<div th:replace="~{fragments/scripts :: scripts}"></div>
</body>
</html>

```

---

## `portfolio-app/src/main/resources/templates/public/index.html`
<a id="portfolio-app-src-main-resources-templates-public-indexhtml"></a>

```html
<!DOCTYPE html>
<!--
  ============================================================================
  TEMPLATE : public/index.html   ->  GET /
  ============================================================================
  The landing page. Sections:
     1. Hero            (photo, name, title, typing animation, buttons)
     2. Statistics      (counted live from the database)
     3. Latest Projects
     4. Top Skills
     5. Services ("What I Do")
     6. Contact

  Every value printed here comes from MySQL - either a table row or a
  site_settings key - so the admin panel can change any of it.
  ============================================================================
-->
<html lang="en" xmlns:th="http://www.thymeleaf.org">

<head th:replace="~{fragments/head :: head('Home')}"></head>

<body>

<!-- Decorative background glow (fixed, behind everything) -->
<div class="bg-glow"></div>

<!-- Navigation -->
<nav th:replace="~{fragments/navbar :: navbar}"></nav>

<main>

    <!-- ==================================================================
         1. HERO
         ================================================================== -->
    <section class="hero">
        <div class="container-px">
            <div class="hero-grid">

                <!-- Left : text -->
                <div>
                    <span class="hero-eyebrow">
                        <i class="bi bi-stars"></i>
                        Available for internships &amp; junior roles
                    </span>

                    <h1 class="hero-title">
                        Hi, I'm <span class="hero-name"
                                      th:text="${settings['hero.name']} ?: 'Vaishnavi Sunil Mali'">Vaishnavi Sunil Mali</span>
                    </h1>

                    <!--
                      The typing animation. The words are supplied by the
                      controller as the "typingWords" list; js/app.js cycles
                      through them. <noscript> shows the plain title instead.
                    -->
                    <div class="hero-typing-line">
                        <span id="typingTarget"
                              th:attr="data-words=${#strings.listJoin(typingWords, '|')}"></span>
                        <span class="cursor"></span>
                    </div>
                    <noscript>
                        <p th:text="${settings['hero.title']} ?: 'EXTC Engineering Student &amp; Developer'">EXTC Engineering Student &amp; Developer</p>
                    </noscript>

                    <p class="hero-intro"
                       th:text="${settings['hero.intro']}">
                        I build clean, reliable Java web applications with Spring Boot and MySQL.
                    </p>

                    <div class="hero-actions">
                        <a th:href="@{${basePrefix != null ? basePrefix : ''} + '/projects'}" class="btn btn-primary btn-lg">
                            <i class="bi bi-collection-play-fill"></i> View My Projects
                        </a>
                        <a th:href="@{${basePrefix != null ? basePrefix : ''} + '/resume'}" class="btn btn-outline btn-lg">
                            <i class="bi bi-file-earmark-pdf-fill"></i> Download Resume
                        </a>
                    </div>

                    <!-- Social links - hidden automatically when a URL is empty -->
                    <div class="hero-socials">
                        <a th:if="${settings['social.github']}"
                           th:href="${settings['social.github']}" target="_blank" rel="noopener"
                           class="btn btn-ghost btn-sm"><i class="bi bi-github"></i> GitHub</a>
                        <a th:if="${settings['social.linkedin']}"
                           th:href="${settings['social.linkedin']}" target="_blank" rel="noopener"
                           class="btn btn-ghost btn-sm"><i class="bi bi-linkedin"></i> LinkedIn</a>
                        <a th:if="${settings['social.twitter']}"
                           th:href="${settings['social.twitter']}" target="_blank" rel="noopener"
                           class="btn btn-ghost btn-sm"><i class="bi bi-twitter-x"></i> Twitter</a>
                        <a th:if="${settings['social.instagram']}"
                           th:href="${settings['social.instagram']}" target="_blank" rel="noopener"
                           class="btn btn-ghost btn-sm"><i class="bi bi-instagram"></i> Instagram</a>
                    </div>
                </div>

                <!-- Right : profile photo with floating stat pills -->
                <div class="hero-avatar-wrap">
                    <img class="hero-avatar"
                         th:src="${settings['profile.image']} ?: @{/img/profile-placeholder.svg}"
                         th:alt="${settings['hero.name']} ?: 'Profile photo'"/>
                    <span class="hero-float f1">
                        <span th:text="${stats['projects']}">0</span> Projects
                    </span>
                    <span class="hero-float f2">
                        <span th:text="${stats['skills']}">0</span> Skills
                    </span>
                </div>
            </div>
        </div>
    </section>

    <!-- ==================================================================
         2. STATISTICS
         ================================================================== -->
    <section class="section-tight">
        <div class="container-px">
            <div class="row-grid">
                <div class="col col-3 reveal">
                    <div class="card-glass stat-card">
                        <div class="stat-value" th:text="${stats['projects']}">0</div>
                        <div class="stat-label">Projects Completed</div>
                    </div>
                </div>
                <div class="col col-3 reveal reveal-delay-1">
                    <div class="card-glass stat-card">
                        <div class="stat-value" th:text="${stats['certifications']}">0</div>
                        <div class="stat-label">Certifications</div>
                    </div>
                </div>
                <div class="col col-3 reveal reveal-delay-2">
                    <div class="card-glass stat-card">
                        <div class="stat-value" th:text="${stats['skills']}">0</div>
                        <div class="stat-label">Technologies</div>
                    </div>
                </div>
                <div class="col col-3 reveal reveal-delay-3">
                    <div class="card-glass stat-card">
                        <div class="stat-value" th:text="${stats['hackathons']}">0</div>
                        <div class="stat-label">Hackathons</div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- ==================================================================
         3. LATEST PROJECTS
         ================================================================== -->
    <section class="section">
        <div class="container-px">
            <div class="section-heading reveal">
                <span class="eyebrow">Portfolio</span>
                <h2>Featured Projects</h2>
                <p>A few of the applications I have designed and built with Java and Spring Boot.</p>
            </div>

            <!-- Empty state - shown only when the admin has deleted everything -->
            <div th:if="${#lists.isEmpty(projects)}" class="empty-state reveal">
                <div class="empty-icon"><i class="bi bi-folder2-open"></i></div>
                <p>No projects have been added yet. Log in to the admin panel to create one.</p>
            </div>

            <div class="row-grid" th:unless="${#lists.isEmpty(projects)}">
                <div class="col col-4 reveal" th:each="project, iter : ${projects}"
                     th:classappend="' reveal-delay-' + ${iter.index + 1}">
                    <div class="card-glass">
                        <div class="project-thumb">
                            <img th:src="${project.imageUrl} ?: @{/img/project-placeholder.svg}"
                                 th:alt="${project.title}"/>
                            <span class="thumb-badge" th:text="${project.category.label}">Java</span>
                        </div>

                        <h3 class="card-title" th:text="${project.title}">Project Title</h3>
                        <p class="card-text" th:text="${project.description}">Short description.</p>

                        <div class="chip-row mb-2">
                            <span class="badge badge-soft"
                                  th:each="tech, t : ${project.technologyList}"
                                  th:if="${t.index < 4}"
                                  th:text="${tech}">Java</span>
                        </div>

                        <div class="project-actions">
                            <a th:href="@{${basePrefix != null ? basePrefix : ''} + '/projects/' + ${project.id}}" class="btn btn-primary btn-sm">
                                <i class="bi bi-eye-fill"></i> View Details
                            </a>
                            <a th:if="${project.githubUrl != null and !project.githubUrl.isBlank()}" th:href="${project.githubUrl}"
                               target="_blank" rel="noopener" class="btn btn-outline btn-sm">
                                <i class="bi bi-github"></i> Code
                            </a>
                        </div>
                    </div>
                </div>
            </div>

            <div class="text-center mt-3">
                <a th:href="@{${basePrefix != null ? basePrefix : ''} + '/projects'}" class="btn btn-outline">
                    View All Projects <i class="bi bi-arrow-right"></i>
                </a>
            </div>
        </div>
    </section>

    <!-- ==================================================================
         4. TOP SKILLS
         ================================================================== -->
    <section class="section section-alt">
        <div class="container-px">
            <div class="section-heading reveal">
                <span class="eyebrow">Expertise</span>
                <h2>Technical Skills</h2>
                <p>The languages, frameworks and tools I use to build software.</p>
            </div>

            <div class="row-grid">
                <div class="col col-6 reveal" th:each="skill, iter : ${skills}"
                     th:classappend="${iter.odd} ? ' reveal-delay-1'">
                    <div class="skill-item">
                        <div class="skill-head">
                            <span class="skill-name" th:text="${skill.name}">Java</span>
                            <span class="skill-pct" th:text="${skill.proficiency} + '%'">90%</span>
                        </div>
                        <div class="progress-track">
                            <div class="progress-fill"
                                 th:classappend="${skill.barClass}"
                                 th:attr="data-width=${skill.proficiency}"></div>
                        </div>
                    </div>
                </div>
            </div>

            <div class="text-center mt-3">
                <a th:href="@{${basePrefix != null ? basePrefix : ''} + '/skills'}" class="btn btn-outline">
                    All Skills <i class="bi bi-arrow-right"></i>
                </a>
            </div>
        </div>
    </section>

    <!-- ==================================================================
         5. SERVICES / WHAT I DO
         ================================================================== -->
    <section class="section" th:unless="${#lists.isEmpty(services)}">
        <div class="container-px">
            <div class="section-heading reveal">
                <span class="eyebrow">What I Do</span>
                <h2>Services</h2>
                <p>Areas where I can help, from backend services to full responsive pages.</p>
            </div>

            <div class="row-grid">
                <div class="col col-3 reveal" th:each="service, iter : ${services}"
                     th:classappend="' reveal-delay-' + ${(iter.index % 4) + 1}">
                    <div class="card-glass">
                        <div class="service-icon">
                            <i th:class="'bi bi-' + ${service.icon}"></i>
                        </div>
                        <h3 class="card-title" th:text="${service.title}">Service</h3>
                        <p class="card-text" th:text="${service.description}">Description.</p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- ==================================================================
         6. CONTACT TEASER
         ================================================================== -->
    <section class="section section-alt">
        <div class="container-px">
            <div class="card-glass reveal" style="text-align:center; padding:44px 26px;">
                <span class="eyebrow"
                      style="background:var(--gradient);-webkit-background-clip:text;background-clip:text;color:transparent;font-weight:700;letter-spacing:.14em;text-transform:uppercase;font-size:.78rem;">
                    Get In Touch
                </span>
                <h2 class="mb-1">Let's build something together</h2>
                <p style="max-width:560px;margin:0 auto 22px;">
                    Have a project idea, an internship opportunity, or just want to talk about Java?
                    Send me a message and I will get back to you.
                </p>
                <a th:href="@{${basePrefix != null ? basePrefix : ''} + '/contact'}" class="btn btn-primary btn-lg">
                    <i class="bi bi-send-fill"></i> Contact Me
                </a>
            </div>
        </div>
    </section>
</main>

<!-- Footer -->
<footer th:replace="~{fragments/footer :: footer}"></footer>

<!-- Back to top button -->
<button id="backToTop" title="Back to top" aria-label="Back to top">
    <i class="bi bi-arrow-up"></i>
</button>

<!-- Toast container -->
<div id="toastContainer"></div>

<!-- Scripts -->
<div th:replace="~{fragments/scripts :: scripts}"></div>

</body>
</html>

```

---

## `portfolio-app/src/main/resources/templates/public/project-details.html`
<a id="portfolio-app-src-main-resources-templates-public-project-detailshtml"></a>

```html
<!DOCTYPE html>
<!--
  ============================================================================
  TEMPLATE : public/project-details.html   ->  GET /projects/{id}
  ============================================================================
  Also reused by the admin preview (GET /admin/projects/view/{id}), which sets
  adminView=true to show an "Edit" button instead of the breadcrumb.

  If the id does not exist, ProjectService throws ResourceNotFoundException and
  GlobalExceptionHandler renders the friendly 404 page instead.
  ============================================================================
-->
<html lang="en" xmlns:th="http://www.thymeleaf.org">
<head th:replace="~{fragments/head :: head(${project.title})}"></head>
<body>

<div class="bg-glow"></div>
<nav th:replace="~{fragments/navbar :: navbar}"></nav>

<main>
    <header class="page-header">
        <div class="container-px">
            <div class="breadcrumb-line">
                <a th:href="@{${basePrefix != null ? basePrefix : ''} + '/'}">Home</a> <span>/</span>
                <a th:href="@{${basePrefix != null ? basePrefix : ''} + '/projects'}">Projects</a> <span>/</span>
                <span th:text="${project.title}">Project</span>
            </div>
            <h1 th:text="${project.title}">Project Title</h1>
            <p th:text="${project.description}">Short description.</p>
            <div class="chip-row mt-2" style="justify-content:center;">
                <span class="badge badge-gradient" th:text="${project.category.label}">Java</span>
                <span class="badge"
                      th:text="'Added ' + ${#temporals.format(project.createdAt, 'dd MMM yyyy')}">
                    Added 01 Jan 2026
                </span>
            </div>
        </div>
    </header>

    <section class="section">
        <div class="container-px">

            <!-- Cover image -->
            <div class="card-glass mb-3 reveal" style="padding:0; overflow:hidden;">
                <img th:src="${project.imageUrl} ?: @{/img/project-placeholder.svg}"
                     th:alt="${project.title}" style="width:100%; border-radius:var(--radius);"/>
            </div>

            <div class="detail-grid">

                <!-- Left column -->
                <div>
                    <!-- Problem statement -->
                    <div class="detail-block mb-2 reveal">
                        <h3><i class="bi bi-question-circle"></i> Problem Statement</h3>
                        <p th:if="${project.problemStatement}" th:text="${project.problemStatement}"
                           style="margin:0;">
                            Problem statement.
                        </p>
                        <p th:unless="${project.problemStatement}" class="text-muted" style="margin:0;">
                            No problem statement was provided for this project.
                        </p>
                    </div>

                    <!-- Features -->
                    <div class="detail-block reveal reveal-delay-1">
                        <h3><i class="bi bi-list-check"></i> Key Features</h3>
                        <ul class="bullet-list" th:unless="${#lists.isEmpty(project.featureList)}">
                            <li th:each="feature : ${project.featureList}" th:text="${feature}">Feature</li>
                        </ul>
                        <p th:if="${#lists.isEmpty(project.featureList)}" class="text-muted" style="margin:0;">
                            No features were listed for this project.
                        </p>
                    </div>
                </div>

                <!-- Right column -->
                <div>
                    <!-- Technologies -->
                    <div class="detail-block mb-2 reveal reveal-delay-1">
                        <h3><i class="bi bi-cpu"></i> Technologies Used</h3>
                        <div class="chip-row">
                            <span class="badge badge-soft"
                                  th:each="tech : ${project.technologyList}"
                                  th:text="${tech}">Java</span>
                        </div>
                    </div>

                    <!-- Links -->
                    <div class="detail-block reveal reveal-delay-2">
                        <h3><i class="bi bi-link-45deg"></i> Links</h3>
                        <div class="gap-row">
                            <a th:if="${project.githubUrl != null and !project.githubUrl.isBlank()}" th:href="${project.githubUrl}"
                               target="_blank" rel="noopener" class="btn btn-outline btn-sm">
                                <i class="bi bi-github"></i> Source Code
                            </a>
                            <a th:if="${project.demoUrl != null and !project.demoUrl.isBlank()}" th:href="${project.demoUrl}"
                               target="_blank" rel="noopener" class="btn btn-primary btn-sm">
                                <i class="bi bi-box-arrow-up-right"></i> Live Demo
                            </a>
                            <span th:if="${(project.githubUrl == null or project.githubUrl.isBlank()) and (project.demoUrl == null or project.demoUrl.isBlank())}"
                                  class="text-muted">Repository and live demo links will be provided upon deployment.</span>
                        </div>
                    </div>

                    <!-- Admin shortcut (only on the admin preview) -->
                    <div class="detail-block reveal reveal-delay-3" th:if="${adminView}" style="margin-top:16px;">
                        <h3><i class="bi bi-shield-lock"></i> Admin</h3>
                        <div class="gap-row">
                            <a th:href="@{'/admin/projects/edit/' + ${project.id}}"
                               class="btn btn-primary btn-sm">
                                <i class="bi bi-pencil-square"></i> Edit Project
                            </a>
                            <a th:href="@{/admin/projects}" class="btn btn-outline btn-sm">
                                <i class="bi bi-arrow-left"></i> Back to List
                            </a>
                        </div>
                    </div>
                </div>
            </div>

            <!-- Related projects -->
            <th:block th:if="${relatedProjects != null and !#lists.isEmpty(relatedProjects)}">
                <div class="divider"></div>
                <div class="section-heading reveal" style="margin-bottom:26px;">
                    <span class="eyebrow">Keep Exploring</span>
                    <h2>More Projects</h2>
                </div>
                <div class="row-grid">
                    <div class="col col-4 reveal" th:each="related : ${relatedProjects}">
                        <div class="card-glass">
                            <div class="project-thumb">
                                <img th:src="${related.imageUrl} ?: @{/img/project-placeholder.svg}"
                                     th:alt="${related.title}" loading="lazy"/>
                            </div>
                            <h3 class="card-title" th:text="${related.title}">Project</h3>
                            <p class="card-text" th:text="${related.description}">Description.</p>
                            <div class="project-actions">
                                <a th:href="@{${basePrefix != null ? basePrefix : ''} + '/projects/' + ${related.id}}"
                                   class="btn btn-outline btn-sm">View Details</a>
                            </div>
                        </div>
                    </div>
                </div>
            </th:block>

            <div class="text-center mt-3">
                <a th:href="@{${basePrefix != null ? basePrefix : ''} + '/projects'}" class="btn btn-outline">
                    <i class="bi bi-arrow-left"></i> Back to All Projects
                </a>
            </div>
        </div>
    </section>
</main>

<footer th:replace="~{fragments/footer :: footer}"></footer>
<button id="backToTop" title="Back to top"><i class="bi bi-arrow-up"></i></button>
<div id="toastContainer"></div>
<div th:replace="~{fragments/scripts :: scripts}"></div>
</body>
</html>

```

---

## `portfolio-app/src/main/resources/templates/public/projects.html`
<a id="portfolio-app-src-main-resources-templates-public-projectshtml"></a>

```html
<!DOCTYPE html>
<!--
  ============================================================================
  TEMPLATE : public/projects.html   ->  GET /projects
  ============================================================================
  TWO WAYS OF FILTERING, BOTH WORKING
    1. Clicking a filter button reloads the page with ?category=JAVA and the
       controller asks the database for that category only. This works with
       JavaScript disabled.
    2. js/app.js also filters the cards already on the page, so the buttons
       feel instant. (Because the server already filtered, both mechanisms
       agree with each other.)

  Each card carries data-category so the JavaScript can show/hide it.
  ============================================================================
-->
<html lang="en" xmlns:th="http://www.thymeleaf.org">
<head th:replace="~{fragments/head :: head('Projects')}"></head>
<body>

<div class="bg-glow"></div>
<nav th:replace="~{fragments/navbar :: navbar}"></nav>

<main>
    <header class="page-header">
        <div class="container-px">
            <div class="breadcrumb-line">
                <a th:href="@{${basePrefix != null ? basePrefix : '/'}}">Home</a> <span>/</span> <span>Projects</span>
            </div>
            <h1>My Projects</h1>
            <p>
                <span th:text="${totalProjects}">0</span> projects built with Java,
                Spring Boot and modern web technologies.
            </p>
        </div>
    </header>

    <section class="section">
        <div class="container-px">

            <!-- FILTER BAR -->
            <div class="filter-bar reveal">
                <a th:href="@{${basePrefix != null ? basePrefix : ''} + '/projects'}"
                   class="filter-btn"
                   th:classappend="${selectedCategory == null} ? ' active'">All</a>
                <a th:each="cat : ${categories}"
                   th:href="@{${basePrefix != null ? basePrefix : ''} + '/projects'(category=${cat})}"
                   class="filter-btn"
                   th:classappend="${selectedCategory != null and selectedCategory == cat} ? ' active'"
                   th:text="${cat.label}">Java</a>
            </div>

            <!-- EMPTY STATE -->
            <div th:if="${#lists.isEmpty(projects)}" class="empty-state reveal">
                <div class="empty-icon"><i class="bi bi-folder2-open"></i></div>
                <p>No projects found in this category yet.</p>
            </div>

            <!-- PROJECT GRID -->
            <div class="row-grid" th:unless="${#lists.isEmpty(projects)}">
                <div class="col col-4 reveal" th:each="project, iter : ${projects}"
                     th:classappend="' reveal-delay-' + ${(iter.index % 3) + 1}"
                     th:attr="data-category=${#strings.toLowerCase(project.category.name())}">

                    <div class="card-glass">
                        <div class="project-thumb">
                            <img th:src="${project.imageUrl} ?: @{/img/project-placeholder.svg}"
                                 th:alt="${project.title}" loading="lazy"/>
                            <span class="thumb-badge" th:text="${project.category.label}">Java</span>
                        </div>

                        <h3 class="card-title" th:text="${project.title}">Project Title</h3>
                        <p class="card-text" th:text="${project.description}">Short description.</p>

                        <div class="chip-row mb-2">
                            <span class="badge badge-soft"
                                  th:each="tech, t : ${project.technologyList}"
                                  th:if="${t.index < 4}"
                                  th:text="${tech}">Java</span>
                            <span class="badge"
                                  th:if="${#lists.size(project.technologyList) > 4}"
                                  th:text="'+' + (${#lists.size(project.technologyList)} - 4) + ' more'">
                                +2 more
                            </span>
                        </div>

                        <div class="project-actions">
                            <a th:href="@{${basePrefix != null ? basePrefix : ''} + '/projects/' + ${project.id}}" class="btn btn-primary btn-sm">
                                <i class="bi bi-eye-fill"></i> View Details
                            </a>
                            <a th:if="${project.githubUrl != null and !project.githubUrl.isBlank()}" th:href="${project.githubUrl}"
                               target="_blank" rel="noopener" class="btn btn-outline btn-sm">
                                <i class="bi bi-github"></i> GitHub
                            </a>
                            <a th:if="${project.demoUrl != null and !project.demoUrl.isBlank()}" th:href="${project.demoUrl}"
                               target="_blank" rel="noopener" class="btn btn-outline btn-sm">
                                <i class="bi bi-box-arrow-up-right"></i> Live Demo
                            </a>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>
</main>

<footer th:replace="~{fragments/footer :: footer}"></footer>
<button id="backToTop" title="Back to top"><i class="bi bi-arrow-up"></i></button>
<div id="toastContainer"></div>
<div th:replace="~{fragments/scripts :: scripts}"></div>
</body>
</html>

```

---

## `portfolio-app/src/main/resources/templates/public/services.html`
<a id="portfolio-app-src-main-resources-templates-public-serviceshtml"></a>

```html
<!DOCTYPE html>
<!--
  ============================================================================
  TEMPLATE : public/services.html   ->  GET /services
  ============================================================================
  The "What I Do" cards. The list arrives as the global model attribute
  "services" (built by GlobalModelAttributes from the services.list setting),
  so no controller code is needed for this page.
  ============================================================================
-->
<html lang="en" xmlns:th="http://www.thymeleaf.org">
<head th:replace="~{fragments/head :: head('Services')}"></head>
<body>

<div class="bg-glow"></div>
<nav th:replace="~{fragments/navbar :: navbar}"></nav>

<main>
    <header class="page-header">
        <div class="container-px">
            <div class="breadcrumb-line">
                <a th:href="@{${basePrefix != null ? basePrefix : '/'}}">Home</a> <span>/</span> <span>Services</span>
            </div>
            <h1>What I Do</h1>
            <p>The kind of work I take on, from backend services to full responsive pages.</p>
        </div>
    </header>

    <section class="section">
        <div class="container-px">

            <div th:if="${#lists.isEmpty(services)}" class="empty-state reveal">
                <div class="empty-icon"><i class="bi bi-grid"></i></div>
                <p>No services configured. Edit them at Admin &rarr; Settings &rarr; Services.</p>
            </div>

            <div class="row-grid" th:unless="${#lists.isEmpty(services)}">
                <div class="col col-4 reveal" th:each="service, iter : ${services}"
                     th:classappend="' reveal-delay-' + ${(iter.index % 3) + 1}">
                    <div class="card-glass">
                        <div class="service-icon">
                            <i th:class="'bi bi-' + ${service.icon}"></i>
                        </div>
                        <h3 class="card-title" th:text="${service.title}">Service</h3>
                        <p class="card-text" th:text="${service.description}">Description.</p>
                    </div>
                </div>
            </div>

            <!-- How I work -->
            <div class="divider"></div>
            <div class="section-heading reveal" style="margin-bottom:30px;">
                <span class="eyebrow">Process</span>
                <h2>How I Work</h2>
            </div>

            <div class="row-grid">
                <div class="col col-3 reveal">
                    <div class="card-glass text-center">
                        <div class="service-icon" style="margin:0 auto 14px;">
                            <i class="bi bi-chat-square-text"></i>
                        </div>
                        <h3 class="card-title">1. Understand</h3>
                        <p class="card-text">Clarify the requirement, scope and success criteria.</p>
                    </div>
                </div>
                <div class="col col-3 reveal reveal-delay-1">
                    <div class="card-glass text-center">
                        <div class="service-icon" style="margin:0 auto 14px;">
                            <i class="bi bi-diagram-3"></i>
                        </div>
                        <h3 class="card-title">2. Design</h3>
                        <p class="card-text">Plan the schema, endpoints and screens before coding.</p>
                    </div>
                </div>
                <div class="col col-3 reveal reveal-delay-2">
                    <div class="card-glass text-center">
                        <div class="service-icon" style="margin:0 auto 14px;">
                            <i class="bi bi-code-slash"></i>
                        </div>
                        <h3 class="card-title">3. Build</h3>
                        <p class="card-text">Write clean, commented code in small reviewable steps.</p>
                    </div>
                </div>
                <div class="col col-3 reveal reveal-delay-3">
                    <div class="card-glass text-center">
                        <div class="service-icon" style="margin:0 auto 14px;">
                            <i class="bi bi-rocket-takeoff"></i>
                        </div>
                        <h3 class="card-title">4. Deliver</h3>
                        <p class="card-text">Test, document and hand over with setup instructions.</p>
                    </div>
                </div>
            </div>

            <div class="text-center mt-3">
                <a th:href="@{${basePrefix != null ? basePrefix : ''} + '/contact'}" class="btn btn-primary btn-lg">
                    <i class="bi bi-send-fill"></i> Start a Conversation
                </a>
            </div>
        </div>
    </section>
</main>

<footer th:replace="~{fragments/footer :: footer}"></footer>
<button id="backToTop" title="Back to top"><i class="bi bi-arrow-up"></i></button>
<div id="toastContainer"></div>
<div th:replace="~{fragments/scripts :: scripts}"></div>
</body>
</html>

```

---

## `portfolio-app/src/main/resources/templates/public/skills.html`
<a id="portfolio-app-src-main-resources-templates-public-skillshtml"></a>

```html
<!DOCTYPE html>
<!--
  ============================================================================
  TEMPLATE : public/skills.html   ->  GET /skills
  ============================================================================
  The controller supplies "groupedSkills": a LinkedHashMap of
      category name  ->  list of Skill
  so one th:each over the map produces one card per category, and a nested
  th:each produces one progress bar per skill.
  ============================================================================
-->
<html lang="en" xmlns:th="http://www.thymeleaf.org">
<head th:replace="~{fragments/head :: head('Skills')}"></head>
<body>

<div class="bg-glow"></div>
<nav th:replace="~{fragments/navbar :: navbar}"></nav>

<main>
    <header class="page-header">
        <div class="container-px">
            <div class="breadcrumb-line">
                <a th:href="@{${basePrefix != null ? basePrefix : '/'}}">Home</a> <span>/</span> <span>Skills</span>
            </div>
            <h1>Technical Skills</h1>
            <p>
                <span th:text="${totalSkills}">0</span> technologies across
                <span th:text="${#maps.size(groupedSkills)}">0</span> categories.
            </p>
        </div>
    </header>

    <section class="section">
        <div class="container-px">

            <div th:if="${#maps.isEmpty(groupedSkills)}" class="empty-state">
                <div class="empty-icon"><i class="bi bi-bar-chart"></i></div>
                <p>No skills have been added yet. Log in to the admin panel to add your skills.</p>
            </div>

            <div class="row-grid">
                <div class="col col-6 reveal" th:each="entry, iter : ${groupedSkills}"
                     th:classappend="${iter.odd} ? ' reveal-delay-1'">
                    <div class="card-glass">
                        <div class="spread mb-2">
                            <h3 class="card-title" style="margin:0;" th:text="${entry.key}">Category</h3>
                            <span class="badge badge-gradient"
                                  th:text="${#lists.size(entry.value)} + ' skills'">5 skills</span>
                        </div>

                        <div class="skill-item" th:each="skill : ${entry.value}">
                            <div class="skill-head">
                                <span class="skill-name" th:text="${skill.name}">Java</span>
                                <span class="skill-pct" th:text="${skill.proficiency} + '%'">90%</span>
                            </div>
                            <div class="progress-track">
                                <div class="progress-fill"
                                     th:classappend="${skill.barClass}"
                                     th:attr="data-width=${skill.proficiency}"></div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>

            <div class="text-center mt-3">
                <a th:href="@{${basePrefix != null ? basePrefix : ''} + '/projects'}" class="btn btn-outline">
                    See these skills in my projects <i class="bi bi-arrow-right"></i>
                </a>
            </div>
        </div>
    </section>
</main>

<footer th:replace="~{fragments/footer :: footer}"></footer>
<button id="backToTop" title="Back to top"><i class="bi bi-arrow-up"></i></button>
<div id="toastContainer"></div>
<div th:replace="~{fragments/scripts :: scripts}"></div>
</body>
</html>

```

---

# 13. Admin Panel Templates

## `portfolio-app/src/main/resources/templates/admin/achievement-form.html`
<a id="portfolio-app-src-main-resources-templates-admin-achievement-formhtml"></a>

```html
<!DOCTYPE html>
<!--
  ============================================================================
  TEMPLATE : admin/achievement-form.html
             ->  GET  /admin/achievements/new
             ->  GET  /admin/achievements/edit/{id}
             ->  POST /admin/achievements/save
  ============================================================================
-->
<html lang="en" xmlns:th="http://www.thymeleaf.org">
<head th:replace="~{fragments/head :: head(${pageTitle})}"></head>
<body>

<div class="bg-glow"></div>

<div class="admin-shell">
    <aside th:replace="~{fragments/admin-sidebar :: sidebar}"></aside>

    <div class="admin-main">
        <header th:replace="~{fragments/admin-topbar :: topbar(${pageTitle})}"></header>

        <div class="admin-content">
            <div th:replace="~{fragments/alerts :: alerts}"></div>

            <div class="panel" style="max-width:800px;">
                <div class="panel-head">
                    <div>
                        <h2 th:text="${pageTitle}">Add Achievement</h2>
                        <p>Hackathons, competitions, awards and academic results.</p>
                    </div>
                    <a th:href="@{/admin/achievements}" class="btn btn-outline btn-sm">
                        <i class="bi bi-arrow-left"></i> Back to List
                    </a>
                </div>

                <form th:action="@{/admin/achievements/save}" th:object="${achievement}" method="post">
                    <input type="hidden" th:field="*{id}"/>

                    <div class="form-group">
                        <label class="form-label" for="title">
                            Achievement Title <span class="req">*</span>
                        </label>
                        <input type="text" class="form-control" id="title"
                               th:field="*{title}" th:errorclass="is-invalid"
                               placeholder="1st Place - Smart Hackathon 2025" maxlength="160" required/>
                        <div class="invalid-feedback" th:if="${#fields.hasErrors('title')}"
                             th:errors="*{title}">Error</div>
                    </div>

                    <div class="form-row">
                        <div class="form-group">
                            <label class="form-label" for="category">Category</label>
                            <select class="form-select" id="category" th:field="*{category}">
                                <option th:each="cat : ${achievementCategories}"
                                        th:value="${cat}" th:text="${cat}">Hackathon</option>
                            </select>
                            <span class="form-text">Decides the badge colour on the public page.</span>
                        </div>

                        <div class="form-group">
                            <label class="form-label" for="achievementDate">Date</label>
                            <input type="date" class="form-control" id="achievementDate"
                                   th:field="*{achievementDate}" th:errorclass="is-invalid"/>
                            <div class="invalid-feedback"
                                 th:if="${#fields.hasErrors('achievementDate')}"
                                 th:errors="*{achievementDate}">Error</div>
                        </div>
                    </div>

                    <div class="form-group">
                        <label class="form-label" for="organization">Organization / Organizer</label>
                        <input type="text" class="form-control" id="organization"
                               th:field="*{organization}" th:errorclass="is-invalid"
                               placeholder="Your College of Engineering" maxlength="160"/>
                        <div class="invalid-feedback" th:if="${#fields.hasErrors('organization')}"
                             th:errors="*{organization}">Error</div>
                    </div>

                    <div class="form-group">
                        <label class="form-label" for="description">Description</label>
                        <textarea class="form-control" id="description" th:field="*{description}"
                                  th:errorclass="is-invalid" data-maxlength="800"
                                  placeholder="What did you build or achieve?"></textarea>
                        <div class="invalid-feedback" th:if="${#fields.hasErrors('description')}"
                             th:errors="*{description}">Error</div>
                    </div>

                    <div class="form-group">
                        <label class="form-label" for="linkUrl">Link (optional)</label>
                        <input type="url" class="form-control" id="linkUrl"
                               th:field="*{linkUrl}" th:errorclass="is-invalid"
                               placeholder="https://results-page.example.com" maxlength="300"/>
                        <div class="invalid-feedback" th:if="${#fields.hasErrors('linkUrl')}"
                             th:errors="*{linkUrl}">Error</div>
                    </div>

                    <div class="form-group">
                        <label class="form-label" for="sortOrder">Display Order</label>
                        <input type="number" class="form-control" id="sortOrder"
                               th:field="*{sortOrder}" min="0" max="999"/>
                    </div>

                    <div class="divider"></div>

                    <div class="gap-row">
                        <button type="submit" class="btn btn-primary">
                            <i class="bi bi-check-lg"></i>
                            <span th:text="${achievement.id == null} ? 'Save Achievement' : 'Update Achievement'">
                                Save
                            </span>
                        </button>
                        <a th:href="@{/admin/achievements}" class="btn btn-outline">Cancel</a>
                    </div>
                </form>
            </div>
        </div>
    </div>
</div>

<div id="toastContainer"></div>
<div th:replace="~{fragments/scripts :: scripts}"></div>
</body>
</html>

```

---

## `portfolio-app/src/main/resources/templates/admin/achievement-list.html`
<a id="portfolio-app-src-main-resources-templates-admin-achievement-listhtml"></a>

```html
<!DOCTYPE html>
<!--
  ============================================================================
  TEMPLATE : admin/achievement-list.html   ->  GET /admin/achievements
  ============================================================================
-->
<html lang="en" xmlns:th="http://www.thymeleaf.org">
<head th:replace="~{fragments/head :: head('Manage Achievements')}"></head>
<body>

<div class="bg-glow"></div>

<div class="admin-shell">
    <aside th:replace="~{fragments/admin-sidebar :: sidebar}"></aside>

    <div class="admin-main">
        <header th:replace="~{fragments/admin-topbar :: topbar('Achievements')}"></header>

        <div class="admin-content">
            <div th:replace="~{fragments/alerts :: alerts}"></div>

            <div class="panel">
                <div class="panel-head">
                    <div>
                        <h2>Achievements</h2>
                        <p><span th:text="${#lists.size(achievements)}">0</span> record(s)</p>
                    </div>
                    <a th:href="@{/admin/achievements/new}" class="btn btn-primary btn-sm">
                        <i class="bi bi-plus-lg"></i> Add Achievement
                    </a>
                </div>

                <div class="toolbar">
                    <form th:action="@{/admin/achievements}" method="get">
                        <input type="search" name="keyword" class="form-control"
                               placeholder="Search title, organization or category..."
                               th:value="${keyword}"/>
                        <button type="submit" class="btn btn-ghost btn-sm">
                            <i class="bi bi-search"></i> Search
                        </button>
                        <a th:href="@{/admin/achievements}" class="btn btn-outline btn-sm">Reset</a>
                    </form>
                </div>

                <div class="table-wrap" th:unless="${#lists.isEmpty(achievements)}">
                    <table class="data-table">
                        <thead>
                        <tr>
                            <th>Title</th>
                            <th style="width:130px;">Category</th>
                            <th>Organization</th>
                            <th style="width:110px;">Date</th>
                            <th style="width:130px;">Actions</th>
                        </tr>
                        </thead>
                        <tbody>
                        <tr th:each="ach : ${achievements}">
                            <td><strong th:text="${ach.title}">Title</strong></td>
                            <td>
                                <span class="badge" th:classappend="${ach.badgeClass}"
                                      th:text="${ach.category}">Award</span>
                            </td>
                            <td th:text="${ach.organization} ?: '-'">Organization</td>
                            <td th:text="${ach.achievementDate != null} ?
                                          ${#temporals.format(ach.achievementDate, 'dd MMM yyyy')} : '-'">
                                01 Jan 2026
                            </td>
                            <td>
                                <div class="action-row">
                                    <a th:href="@{'/admin/achievements/edit/' + ${ach.id}}"
                                       class="btn btn-warning btn-sm" title="Edit">
                                        <i class="bi bi-pencil"></i>
                                    </a>
                                    <form th:action="@{'/admin/achievements/delete/' + ${ach.id}}"
                                          method="post"
                                          th:attr="data-confirm='Delete \'' + ${ach.title} + '\'?',
                                                   data-confirm-title='Delete Achievement'">
                                        <button type="submit" class="btn btn-danger btn-sm" title="Delete">
                                            <i class="bi bi-trash"></i>
                                        </button>
                                    </form>
                                </div>
                            </td>
                        </tr>
                        </tbody>
                    </table>
                </div>

                <div th:if="${#lists.isEmpty(achievements)}" class="empty-state">
                    <div class="empty-icon"><i class="bi bi-trophy"></i></div>
                    <p>No achievements yet.</p>
                </div>
            </div>
        </div>
    </div>
</div>

<div id="toastContainer"></div>
<div th:replace="~{fragments/scripts :: scripts}"></div>
</body>
</html>

```

---

## `portfolio-app/src/main/resources/templates/admin/certification-form.html`
<a id="portfolio-app-src-main-resources-templates-admin-certification-formhtml"></a>

```html
<!DOCTYPE html>
<!--
  ============================================================================
  TEMPLATE : admin/certification-form.html
             ->  GET  /admin/certifications/new
             ->  GET  /admin/certifications/edit/{id}
             ->  POST /admin/certifications/save
  ============================================================================
  You can either UPLOAD a certificate image/PDF or paste a link to it.
  When a file is uploaded and no link is given, the uploaded file becomes the
  "View Certificate" target automatically (see AdminCertificationController).
  ============================================================================
-->
<html lang="en" xmlns:th="http://www.thymeleaf.org">
<head th:replace="~{fragments/head :: head(${pageTitle})}"></head>
<body>

<div class="bg-glow"></div>

<div class="admin-shell">
    <aside th:replace="~{fragments/admin-sidebar :: sidebar}"></aside>

    <div class="admin-main">
        <header th:replace="~{fragments/admin-topbar :: topbar(${pageTitle})}"></header>

        <div class="admin-content">
            <div th:replace="~{fragments/alerts :: alerts}"></div>

            <div class="panel" style="max-width:800px;">
                <div class="panel-head">
                    <div>
                        <h2 th:text="${pageTitle}">Add Certification</h2>
                        <p>Add a course or certification you have completed.</p>
                    </div>
                    <a th:href="@{/admin/certifications}" class="btn btn-outline btn-sm">
                        <i class="bi bi-arrow-left"></i> Back to List
                    </a>
                </div>

                <form th:action="@{/admin/certifications/save}" th:object="${certification}"
                      method="post" enctype="multipart/form-data">
                    <input type="hidden" th:field="*{id}"/>
                    <input type="hidden" th:field="*{imageUrl}"/>

                    <div class="form-group">
                        <label class="form-label" for="title">
                            Certificate Title <span class="req">*</span>
                        </label>
                        <input type="text" class="form-control" id="title"
                               th:field="*{title}" th:errorclass="is-invalid"
                               placeholder="Programming in Java" maxlength="160" required/>
                        <div class="invalid-feedback" th:if="${#fields.hasErrors('title')}"
                             th:errors="*{title}">Error</div>
                    </div>

                    <div class="form-row">
                        <div class="form-group">
                            <label class="form-label" for="issuer">
                                Issuing Organization <span class="req">*</span>
                            </label>
                            <input type="text" class="form-control" id="issuer"
                                   th:field="*{issuer}" th:errorclass="is-invalid"
                                   placeholder="Oracle / Coursera / NPTEL" maxlength="120" required/>
                            <div class="invalid-feedback" th:if="${#fields.hasErrors('issuer')}"
                                 th:errors="*{issuer}">Error</div>
                        </div>

                        <div class="form-group">
                            <label class="form-label" for="issueDate">Issue Date</label>
                            <input type="date" class="form-control" id="issueDate"
                                   th:field="*{issueDate}" th:errorclass="is-invalid"/>
                            <div class="invalid-feedback" th:if="${#fields.hasErrors('issueDate')}"
                                 th:errors="*{issueDate}">Error</div>
                        </div>
                    </div>

                    <div class="form-group">
                        <label class="form-label" for="credentialId">Credential ID</label>
                        <input type="text" class="form-control" id="credentialId"
                               th:field="*{credentialId}" placeholder="CERT-0001" maxlength="60"/>
                    </div>

                    <div class="form-group">
                        <label class="form-label" for="certificateUrl">Certificate Link (PDF or verification page)</label>
                        <input type="url" class="form-control" id="certificateUrl"
                               th:field="*{certificateUrl}" th:errorclass="is-invalid"
                               placeholder="https://your-certificate-link.example.com/abc" maxlength="300"/>
                        <div class="invalid-feedback" th:if="${#fields.hasErrors('certificateUrl')}"
                             th:errors="*{certificateUrl}">Error</div>
                    </div>

                    <div class="form-group">
                        <label class="form-label" for="imageFile">Upload Certificate Image / PDF</label>
                        <input type="file" class="form-control" id="imageFile" name="imageFile"
                               accept="image/png,image/jpeg,image/webp,image/gif,application/pdf"/>
                        <span class="form-text">PNG, JPG, WEBP, GIF or PDF - maximum 5 MB.</span>
                        <div class="mt-1" th:if="${certification.imageUrl}">
                            <img th:if="${!#strings.endsWith(certification.imageUrl, '.pdf')}"
                                 th:src="${certification.imageUrl}" alt="Current certificate image"
                                 style="width:170px; border-radius:9px; border:1px solid var(--border-color);"/>
                            <div class="form-text">
                                Current file: <span th:text="${certification.imageUrl}">/uploads/...</span>
                            </div>
                        </div>
                        <div class="invalid-feedback" th:if="${#fields.hasErrors('imageUrl')}"
                             th:errors="*{imageUrl}">Error</div>
                    </div>

                    <div class="form-group">
                        <label class="form-label" for="sortOrder">Display Order</label>
                        <input type="number" class="form-control" id="sortOrder"
                               th:field="*{sortOrder}" min="0" max="999"/>
                    </div>

                    <div class="divider"></div>

                    <div class="gap-row">
                        <button type="submit" class="btn btn-primary">
                            <i class="bi bi-check-lg"></i>
                            <span th:text="${certification.id == null} ? 'Save Certification' : 'Update Certification'">
                                Save
                            </span>
                        </button>
                        <a th:href="@{/admin/certifications}" class="btn btn-outline">Cancel</a>
                    </div>
                </form>
            </div>
        </div>
    </div>
</div>

<div id="toastContainer"></div>
<div th:replace="~{fragments/scripts :: scripts}"></div>
</body>
</html>

```

---

## `portfolio-app/src/main/resources/templates/admin/certification-list.html`
<a id="portfolio-app-src-main-resources-templates-admin-certification-listhtml"></a>

```html
<!DOCTYPE html>
<!--
  ============================================================================
  TEMPLATE : admin/certification-list.html   ->  GET /admin/certifications
  ============================================================================
-->
<html lang="en" xmlns:th="http://www.thymeleaf.org">
<head th:replace="~{fragments/head :: head('Manage Certifications')}"></head>
<body>

<div class="bg-glow"></div>

<div class="admin-shell">
    <aside th:replace="~{fragments/admin-sidebar :: sidebar}"></aside>

    <div class="admin-main">
        <header th:replace="~{fragments/admin-topbar :: topbar('Certifications')}"></header>

        <div class="admin-content">
            <div th:replace="~{fragments/alerts :: alerts}"></div>

            <div class="panel">
                <div class="panel-head">
                    <div>
                        <h2>Certifications</h2>
                        <p><span th:text="${#lists.size(certifications)}">0</span> certificate(s)</p>
                    </div>
                    <a th:href="@{/admin/certifications/new}" class="btn btn-primary btn-sm">
                        <i class="bi bi-plus-lg"></i> Add Certification
                    </a>
                </div>

                <div class="toolbar">
                    <form th:action="@{/admin/certifications}" method="get">
                        <input type="search" name="keyword" class="form-control"
                               placeholder="Search title or issuer..." th:value="${keyword}"/>
                        <button type="submit" class="btn btn-ghost btn-sm">
                            <i class="bi bi-search"></i> Search
                        </button>
                        <a th:href="@{/admin/certifications}" class="btn btn-outline btn-sm">Reset</a>
                    </form>
                </div>

                <div class="table-wrap" th:unless="${#lists.isEmpty(certifications)}">
                    <table class="data-table">
                        <thead>
                        <tr>
                            <th style="width:70px;">Image</th>
                            <th>Title</th>
                            <th>Issuer</th>
                            <th style="width:110px;">Date</th>
                            <th style="width:130px;">Credential</th>
                            <th style="width:170px;">Actions</th>
                        </tr>
                        </thead>
                        <tbody>
                        <tr th:each="cert : ${certifications}">
                            <td>
                                <img th:src="${cert.imageUrl} ?: @{/img/certificate-placeholder.svg}"
                                     th:alt="${cert.title}"
                                     style="width:56px; height:42px; object-fit:cover; border-radius:7px;"/>
                            </td>
                            <td><strong th:text="${cert.title}">Title</strong></td>
                            <td th:text="${cert.issuer}">Issuer</td>
                            <td th:text="${cert.issueDate != null} ?
                                          ${#temporals.format(cert.issueDate, 'dd MMM yyyy')} : '-'">
                                01 Jan 2026
                            </td>
                            <td>
                                <span class="badge" th:if="${cert.credentialId}"
                                      th:text="${cert.credentialId}">CERT-0001</span>
                            </td>
                            <td>
                                <div class="action-row">
                                    <a th:if="${cert.certificateUrl}" th:href="${cert.certificateUrl}"
                                       target="_blank" rel="noopener"
                                       class="btn btn-ghost btn-sm" title="Open certificate">
                                        <i class="bi bi-box-arrow-up-right"></i>
                                    </a>
                                    <a th:href="@{'/admin/certifications/edit/' + ${cert.id}}"
                                       class="btn btn-warning btn-sm" title="Edit">
                                        <i class="bi bi-pencil"></i>
                                    </a>
                                    <form th:action="@{'/admin/certifications/delete/' + ${cert.id}}"
                                          method="post"
                                          th:attr="data-confirm='Delete \'' + ${cert.title} + '\'?',
                                                   data-confirm-title='Delete Certification'">
                                        <button type="submit" class="btn btn-danger btn-sm" title="Delete">
                                            <i class="bi bi-trash"></i>
                                        </button>
                                    </form>
                                </div>
                            </td>
                        </tr>
                        </tbody>
                    </table>
                </div>

                <div th:if="${#lists.isEmpty(certifications)}" class="empty-state">
                    <div class="empty-icon"><i class="bi bi-patch-check"></i></div>
                    <p>No certifications yet.</p>
                </div>
            </div>
        </div>
    </div>
</div>

<div id="toastContainer"></div>
<div th:replace="~{fragments/scripts :: scripts}"></div>
</body>
</html>

```

---

## `portfolio-app/src/main/resources/templates/admin/dashboard.html`
<a id="portfolio-app-src-main-resources-templates-admin-dashboardhtml"></a>

```html
<!DOCTYPE html>
<!--
  ============================================================================
  TEMPLATE : admin/dashboard.html   ->  GET /admin/dashboard
  ============================================================================
  Protected by Spring Security: an anonymous visitor asking for this URL is
  redirected to /admin/login before this template is ever rendered.

  "stats" is the DashboardStats record built by DashboardService.
  ============================================================================
-->
<html lang="en" xmlns:th="http://www.thymeleaf.org"
      xmlns:sec="http://www.thymeleaf.org/extras/spring-security">
<head th:replace="~{fragments/head :: head('Admin Dashboard')}"></head>
<body>

<div class="bg-glow"></div>

<div class="admin-shell">

    <!-- SIDEBAR -->
    <aside th:replace="~{fragments/admin-sidebar :: sidebar}"></aside>

    <!-- MAIN -->
    <div class="admin-main">
        <header th:replace="~{fragments/admin-topbar :: topbar('Dashboard')}"></header>

        <div class="admin-content">

            <div th:replace="~{fragments/alerts :: alerts}"></div>

            <!-- Welcome strip -->
            <div class="panel">
                <div class="spread">
                    <div>
                        <h2 style="margin-bottom:4px;">
                            Welcome back,
                            <span sec:authentication="name">admin</span>
                        </h2>
                        <p style="margin:0;">
                            Everything on your public website is managed from here.
                            Changes appear on the site immediately after saving.
                        </p>
                    </div>
                    <div class="gap-row">
                        <a th:href="@{/admin/projects/new}" class="btn btn-primary btn-sm">
                            <i class="bi bi-plus-lg"></i> Add Project
                        </a>
                        <a th:href="@{/admin/settings}" class="btn btn-outline btn-sm">
                            <i class="bi bi-person-gear"></i> Edit Profile
                        </a>
                    </div>
                </div>
            </div>

            <!-- STAT TILES -->
            <div class="stat-grid">
                <div class="stat-tile">
                    <div class="tile-icon c1"><i class="bi bi-folder-fill"></i></div>
                    <div>
                        <div class="tile-value" th:text="${stats.totalProjects}">0</div>
                        <div class="tile-label">Projects</div>
                    </div>
                </div>
                <div class="stat-tile">
                    <div class="tile-icon c2"><i class="bi bi-bar-chart-fill"></i></div>
                    <div>
                        <div class="tile-value" th:text="${stats.totalSkills}">0</div>
                        <div class="tile-label">Skills</div>
                    </div>
                </div>
                <div class="stat-tile">
                    <div class="tile-icon c5"><i class="bi bi-patch-check-fill"></i></div>
                    <div>
                        <div class="tile-value" th:text="${stats.totalCertifications}">0</div>
                        <div class="tile-label">Certificates</div>
                    </div>
                </div>
                <div class="stat-tile">
                    <div class="tile-icon c4"><i class="bi bi-trophy-fill"></i></div>
                    <div>
                        <div class="tile-value" th:text="${stats.totalAchievements}">0</div>
                        <div class="tile-label">Achievements</div>
                    </div>
                </div>
                <div class="stat-tile">
                    <div class="tile-icon c7"><i class="bi bi-briefcase-fill"></i></div>
                    <div>
                        <div class="tile-value" th:text="${stats.totalExperiences}">0</div>
                        <div class="tile-label">Experiences</div>
                    </div>
                </div>
                <div class="stat-tile">
                    <div class="tile-icon c3"><i class="bi bi-mortarboard-fill"></i></div>
                    <div>
                        <div class="tile-value" th:text="${stats.totalEducations}">0</div>
                        <div class="tile-label">Education</div>
                    </div>
                </div>
                <div class="stat-tile">
                    <div class="tile-icon c6"><i class="bi bi-envelope-fill"></i></div>
                    <div>
                        <div class="tile-value" th:text="${stats.totalMessages}">0</div>
                        <div class="tile-label">Messages</div>
                    </div>
                </div>
                <div class="stat-tile">
                    <div class="tile-icon c8"><i class="bi bi-exclamation-circle-fill"></i></div>
                    <div>
                        <div class="tile-value" th:text="${stats.unreadMessages}">0</div>
                        <div class="tile-label">Unread</div>
                    </div>
                </div>
            </div>

            <!-- RECENT ACTIVITY -->
            <div class="admin-grid-2">

                <!-- Recent projects -->
                <div class="panel">
                    <div class="panel-head">
                        <div>
                            <h2>Recent Projects</h2>
                            <p>The newest entries in your portfolio</p>
                        </div>
                        <a th:href="@{/admin/projects}" class="btn btn-ghost btn-sm">Manage</a>
                    </div>

                    <ul class="mini-list" th:unless="${#lists.isEmpty(recentProjects)}">
                        <li th:each="project : ${recentProjects}">
                            <span class="mini-title" th:text="${project.title}">Project</span>
                            <span class="badge" th:text="${project.category.label}">Java</span>
                        </li>
                    </ul>
                    <p th:if="${#lists.isEmpty(recentProjects)}" class="text-muted">
                        No projects yet.
                    </p>
                </div>

                <!-- Recent messages -->
                <div class="panel">
                    <div class="panel-head">
                        <div>
                            <h2>Latest Messages</h2>
                            <p>Contact form submissions</p>
                        </div>
                        <a th:href="@{/admin/messages}" class="btn btn-ghost btn-sm">Inbox</a>
                    </div>

                    <ul class="mini-list" th:unless="${#lists.isEmpty(recentMessages)}">
                        <li th:each="message : ${recentMessages}">
                            <span class="mini-title">
                                <span th:if="${!message.readStatus}"
                                      style="color:#ff8b96; font-weight:800;">&#9679; </span>
                                <span th:text="${message.subject}">Subject</span>
                            </span>
                            <span class="mini-meta" th:text="${message.name}">Name</span>
                        </li>
                    </ul>
                    <p th:if="${#lists.isEmpty(recentMessages)}" class="text-muted">
                        No messages yet.
                    </p>
                </div>

                <!-- Recent skills -->
                <div class="panel">
                    <div class="panel-head">
                        <div>
                            <h2>Skills</h2>
                            <p>First few of your listed skills</p>
                        </div>
                        <a th:href="@{/admin/skills}" class="btn btn-ghost btn-sm">Manage</a>
                    </div>

                    <ul class="mini-list" th:unless="${#lists.isEmpty(recentSkills)}">
                        <li th:each="skill : ${recentSkills}">
                            <span class="mini-title" th:text="${skill.name}">Skill</span>
                            <span class="mini-meta" th:text="${skill.proficiency} + '%'">80%</span>
                        </li>
                    </ul>
                    <p th:if="${#lists.isEmpty(recentSkills)}" class="text-muted">No skills yet.</p>
                </div>

                <!-- Certifications + achievements -->
                <div class="panel">
                    <div class="panel-head">
                        <div>
                            <h2>Certificates &amp; Achievements</h2>
                            <p>Recent additions</p>
                        </div>
                        <div class="gap-row">
                            <a th:href="@{/admin/certifications}" class="btn btn-ghost btn-sm">Certs</a>
                            <a th:href="@{/admin/achievements}" class="btn btn-ghost btn-sm">Awards</a>
                        </div>
                    </div>

                    <ul class="mini-list">
                        <li th:each="cert : ${recentCertifications}">
                            <span class="mini-title" th:text="${cert.title}">Certificate</span>
                            <span class="badge badge-info">Certificate</span>
                        </li>
                        <li th:each="ach : ${recentAchievements}">
                            <span class="mini-title" th:text="${ach.title}">Achievement</span>
                            <span class="badge" th:classappend="${ach.badgeClass}"
                                  th:text="${ach.category}">Award</span>
                        </li>
                    </ul>
                    <p th:if="${#lists.isEmpty(recentCertifications) and #lists.isEmpty(recentAchievements)}"
                       class="text-muted">Nothing added yet.</p>
                </div>
            </div>

            <!-- Quick links -->
            <div class="panel">
                <div class="panel-head">
                    <div>
                        <h2>Quick Actions</h2>
                        <p>Jump straight to the most common tasks</p>
                    </div>
                </div>
                <div class="gap-row">
                    <a th:href="@{/admin/projects/new}" class="btn btn-outline btn-sm">
                        <i class="bi bi-plus-circle"></i> New Project
                    </a>
                    <a th:href="@{/admin/skills/new}" class="btn btn-outline btn-sm">
                        <i class="bi bi-plus-circle"></i> New Skill
                    </a>
                    <a th:href="@{/admin/certifications/new}" class="btn btn-outline btn-sm">
                        <i class="bi bi-plus-circle"></i> New Certificate
                    </a>
                    <a th:href="@{/admin/achievements/new}" class="btn btn-outline btn-sm">
                        <i class="bi bi-plus-circle"></i> New Achievement
                    </a>
                    <a th:href="@{/admin/messages(unreadOnly=true)}" class="btn btn-outline btn-sm">
                        <i class="bi bi-envelope"></i> Unread Messages
                    </a>
                    <a th:href="@{/api/projects}" target="_blank" class="btn btn-outline btn-sm">
                        <i class="bi bi-braces"></i> JSON API
                    </a>
                </div>
            </div>
        </div>
    </div>
</div>

<div id="toastContainer"></div>
<div th:replace="~{fragments/scripts :: scripts}"></div>
</body>
</html>

```

---

## `portfolio-app/src/main/resources/templates/admin/education-form.html`
<a id="portfolio-app-src-main-resources-templates-admin-education-formhtml"></a>

```html
<!DOCTYPE html>
<!--
  ============================================================================
  TEMPLATE : admin/education-form.html
             ->  GET  /admin/education/new
             ->  GET  /admin/education/edit/{id}
             ->  POST /admin/education/save
  ============================================================================
-->
<html lang="en" xmlns:th="http://www.thymeleaf.org">
<head th:replace="~{fragments/head :: head(${pageTitle})}"></head>
<body>

<div class="bg-glow"></div>

<div class="admin-shell">
    <aside th:replace="~{fragments/admin-sidebar :: sidebar}"></aside>

    <div class="admin-main">
        <header th:replace="~{fragments/admin-topbar :: topbar(${pageTitle})}"></header>

        <div class="admin-content">
            <div th:replace="~{fragments/alerts :: alerts}"></div>

            <div class="panel" style="max-width:760px;">
                <div class="panel-head">
                    <div>
                        <h2 th:text="${pageTitle}">Add Education Entry</h2>
                        <p>Shown on the public Education timeline.</p>
                    </div>
                    <a th:href="@{/admin/education}" class="btn btn-outline btn-sm">
                        <i class="bi bi-arrow-left"></i> Back to List
                    </a>
                </div>

                <form th:action="@{/admin/education/save}" th:object="${education}" method="post">
                    <input type="hidden" th:field="*{id}"/>

                    <div class="form-group">
                        <label class="form-label" for="degree">
                            Degree / Qualification <span class="req">*</span>
                        </label>
                        <input type="text" class="form-control" id="degree"
                               th:field="*{degree}" th:errorclass="is-invalid"
                               placeholder="B.E. Computer Engineering" maxlength="120" required/>
                        <div class="invalid-feedback" th:if="${#fields.hasErrors('degree')}"
                             th:errors="*{degree}">Error</div>
                    </div>

                    <div class="form-group">
                        <label class="form-label" for="institution">
                            Institution <span class="req">*</span>
                        </label>
                        <input type="text" class="form-control" id="institution"
                               th:field="*{institution}" th:errorclass="is-invalid"
                               placeholder="Your College of Engineering, Your City"
                               maxlength="160" required/>
                        <div class="invalid-feedback" th:if="${#fields.hasErrors('institution')}"
                             th:errors="*{institution}">Error</div>
                    </div>

                    <div class="form-row">
                        <div class="form-group">
                            <label class="form-label" for="startYear">
                                Start Year <span class="req">*</span>
                            </label>
                            <input type="number" class="form-control" id="startYear"
                                   th:field="*{startYear}" th:errorclass="is-invalid"
                                   min="1950" max="2100" required/>
                            <div class="invalid-feedback" th:if="${#fields.hasErrors('startYear')}"
                                 th:errors="*{startYear}">Error</div>
                        </div>

                        <div class="form-group">
                            <label class="form-label" for="endYear">
                                End Year <span class="req">*</span>
                            </label>
                            <input type="number" class="form-control" id="endYear"
                                   th:field="*{endYear}" th:errorclass="is-invalid"
                                   min="1950" max="2100" required/>
                            <div class="invalid-feedback" th:if="${#fields.hasErrors('endYear')}"
                                 th:errors="*{endYear}">Error</div>
                        </div>

                        <div class="form-group">
                            <label class="form-label" for="percentageOrCgpa">CGPA / Percentage</label>
                            <input type="text" class="form-control" id="percentageOrCgpa"
                                   th:field="*{percentageOrCgpa}" th:errorclass="is-invalid"
                                   placeholder="8.70 CGPA" maxlength="30"/>
                            <div class="invalid-feedback"
                                 th:if="${#fields.hasErrors('percentageOrCgpa')}"
                                 th:errors="*{percentageOrCgpa}">Error</div>
                        </div>
                    </div>

                    <div class="form-group">
                        <label class="form-label" for="description">Description</label>
                        <textarea class="form-control" id="description"
                                  th:field="*{description}" th:errorclass="is-invalid"
                                  data-maxlength="600"
                                  placeholder="Specialisation, important coursework, activities..."></textarea>
                        <div class="invalid-feedback" th:if="${#fields.hasErrors('description')}"
                             th:errors="*{description}">Error</div>
                    </div>

                    <div class="form-group">
                        <label class="form-label" for="sortOrder">Display Order</label>
                        <input type="number" class="form-control" id="sortOrder"
                               th:field="*{sortOrder}" min="0" max="999"/>
                    </div>

                    <div class="divider"></div>

                    <div class="gap-row">
                        <button type="submit" class="btn btn-primary">
                            <i class="bi bi-check-lg"></i>
                            <span th:text="${education.id == null} ? 'Save Entry' : 'Update Entry'">Save</span>
                        </button>
                        <a th:href="@{/admin/education}" class="btn btn-outline">Cancel</a>
                    </div>
                </form>
            </div>
        </div>
    </div>
</div>

<div id="toastContainer"></div>
<div th:replace="~{fragments/scripts :: scripts}"></div>
</body>
</html>

```

---

## `portfolio-app/src/main/resources/templates/admin/education-list.html`
<a id="portfolio-app-src-main-resources-templates-admin-education-listhtml"></a>

```html
<!DOCTYPE html>
<!--
  ============================================================================
  TEMPLATE : admin/education-list.html   ->  GET /admin/education
  ============================================================================
-->
<html lang="en" xmlns:th="http://www.thymeleaf.org">
<head th:replace="~{fragments/head :: head('Manage Education')}"></head>
<body>

<div class="bg-glow"></div>

<div class="admin-shell">
    <aside th:replace="~{fragments/admin-sidebar :: sidebar}"></aside>

    <div class="admin-main">
        <header th:replace="~{fragments/admin-topbar :: topbar('Education')}"></header>

        <div class="admin-content">
            <div th:replace="~{fragments/alerts :: alerts}"></div>

            <div class="panel">
                <div class="panel-head">
                    <div>
                        <h2>Education Entries</h2>
                        <p><span th:text="${#lists.size(educations)}">0</span> record(s)</p>
                    </div>
                    <a th:href="@{/admin/education/new}" class="btn btn-primary btn-sm">
                        <i class="bi bi-plus-lg"></i> Add Education
                    </a>
                </div>

                <div class="toolbar">
                    <form th:action="@{/admin/education}" method="get">
                        <input type="search" name="keyword" class="form-control"
                               placeholder="Search degree or institution..." th:value="${keyword}"/>
                        <button type="submit" class="btn btn-ghost btn-sm">
                            <i class="bi bi-search"></i> Search
                        </button>
                        <a th:href="@{/admin/education}" class="btn btn-outline btn-sm">Reset</a>
                    </form>
                </div>

                <div class="table-wrap" th:unless="${#lists.isEmpty(educations)}">
                    <table class="data-table">
                        <thead>
                        <tr>
                            <th>Degree</th>
                            <th>Institution</th>
                            <th style="width:120px;">Years</th>
                            <th style="width:120px;">Result</th>
                            <th style="width:130px;">Actions</th>
                        </tr>
                        </thead>
                        <tbody>
                        <tr th:each="edu : ${educations}">
                            <td><strong th:text="${edu.degree}">Degree</strong></td>
                            <td th:text="${edu.institution}">Institution</td>
                            <td th:text="${edu.yearRange}">2022 - 2026</td>
                            <td>
                                <span class="badge badge-soft" th:if="${edu.percentageOrCgpa}"
                                      th:text="${edu.percentageOrCgpa}">8.70 CGPA</span>
                            </td>
                            <td>
                                <div class="action-row">
                                    <a th:href="@{'/admin/education/edit/' + ${edu.id}}"
                                       class="btn btn-warning btn-sm" title="Edit">
                                        <i class="bi bi-pencil"></i>
                                    </a>
                                    <form th:action="@{'/admin/education/delete/' + ${edu.id}}"
                                          method="post"
                                          th:attr="data-confirm='Delete \'' + ${edu.degree} + '\'?',
                                                   data-confirm-title='Delete Education'">
                                        <button type="submit" class="btn btn-danger btn-sm" title="Delete">
                                            <i class="bi bi-trash"></i>
                                        </button>
                                    </form>
                                </div>
                            </td>
                        </tr>
                        </tbody>
                    </table>
                </div>

                <div th:if="${#lists.isEmpty(educations)}" class="empty-state">
                    <div class="empty-icon"><i class="bi bi-mortarboard"></i></div>
                    <p>No education entries yet.</p>
                </div>
            </div>
        </div>
    </div>
</div>

<div id="toastContainer"></div>
<div th:replace="~{fragments/scripts :: scripts}"></div>
</body>
</html>

```

---

## `portfolio-app/src/main/resources/templates/admin/experience-form.html`
<a id="portfolio-app-src-main-resources-templates-admin-experience-formhtml"></a>

```html
<!DOCTYPE html>
<!--
  ============================================================================
  TEMPLATE : admin/experience-form.html
             ->  GET  /admin/experience/new
             ->  GET  /admin/experience/edit/{id}
             ->  POST /admin/experience/save
  ============================================================================
  Leaving the End Date empty means "I still work here", and the public page
  prints "Present" (see Experience.getDateRange()).
  ============================================================================
-->
<html lang="en" xmlns:th="http://www.thymeleaf.org">
<head th:replace="~{fragments/head :: head(${pageTitle})}"></head>
<body>

<div class="bg-glow"></div>

<div class="admin-shell">
    <aside th:replace="~{fragments/admin-sidebar :: sidebar}"></aside>

    <div class="admin-main">
        <header th:replace="~{fragments/admin-topbar :: topbar(${pageTitle})}"></header>

        <div class="admin-content">
            <div th:replace="~{fragments/alerts :: alerts}"></div>

            <div class="panel" style="max-width:800px;">
                <div class="panel-head">
                    <div>
                        <h2 th:text="${pageTitle}">Add Experience Entry</h2>
                        <p>Internships, jobs and roles.</p>
                    </div>
                    <a th:href="@{/admin/experience}" class="btn btn-outline btn-sm">
                        <i class="bi bi-arrow-left"></i> Back to List
                    </a>
                </div>

                <form th:action="@{/admin/experience/save}" th:object="${experience}" method="post">
                    <input type="hidden" th:field="*{id}"/>

                    <div class="form-row">
                        <div class="form-group">
                            <label class="form-label" for="position">
                                Position / Role <span class="req">*</span>
                            </label>
                            <input type="text" class="form-control" id="position"
                                   th:field="*{position}" th:errorclass="is-invalid"
                                   placeholder="Java Developer Intern" maxlength="120" required/>
                            <div class="invalid-feedback" th:if="${#fields.hasErrors('position')}"
                                 th:errors="*{position}">Error</div>
                        </div>

                        <div class="form-group">
                            <label class="form-label" for="organization">
                                Organization <span class="req">*</span>
                            </label>
                            <input type="text" class="form-control" id="organization"
                                   th:field="*{organization}" th:errorclass="is-invalid"
                                   placeholder="Your Company Name Pvt. Ltd." maxlength="160" required/>
                            <div class="invalid-feedback" th:if="${#fields.hasErrors('organization')}"
                                 th:errors="*{organization}">Error</div>
                        </div>
                    </div>

                    <div class="form-row">
                        <div class="form-group">
                            <label class="form-label" for="startDate">Start Date</label>
                            <input type="date" class="form-control" id="startDate"
                                   th:field="*{startDate}" th:errorclass="is-invalid"/>
                            <div class="invalid-feedback" th:if="${#fields.hasErrors('startDate')}"
                                 th:errors="*{startDate}">Error</div>
                        </div>

                        <div class="form-group">
                            <label class="form-label" for="endDate">End Date</label>
                            <input type="date" class="form-control" id="endDate"
                                   th:field="*{endDate}" th:errorclass="is-invalid"/>
                            <span class="form-text">Leave empty for a current role ("Present").</span>
                            <div class="invalid-feedback" th:if="${#fields.hasErrors('endDate')}"
                                 th:errors="*{endDate}">Error</div>
                        </div>
                    </div>

                    <div class="form-group">
                        <label class="form-label" for="description">Responsibilities</label>
                        <textarea class="form-control" id="description" th:field="*{description}"
                                  style="min-height:160px;"
                                  placeholder="One responsibility per line:&#10;Developed and tested REST endpoints&#10;Wrote JPA repositories&#10;Fixed defects from the testing cycle"></textarea>
                        <span class="form-text">One responsibility per line - each becomes a bullet.</span>
                    </div>

                    <div class="form-group">
                        <label class="form-label" for="technologies">Technologies</label>
                        <input type="text" class="form-control" id="technologies"
                               th:field="*{technologies}" th:errorclass="is-invalid"
                               placeholder="Java, Spring Boot, MySQL, Git" maxlength="300"/>
                        <span class="form-text">Comma separated.</span>
                        <div class="invalid-feedback" th:if="${#fields.hasErrors('technologies')}"
                             th:errors="*{technologies}">Error</div>
                    </div>

                    <div class="form-group">
                        <label class="form-label" for="sortOrder">Display Order</label>
                        <input type="number" class="form-control" id="sortOrder"
                               th:field="*{sortOrder}" min="0" max="999"/>
                    </div>

                    <div class="divider"></div>

                    <div class="gap-row">
                        <button type="submit" class="btn btn-primary">
                            <i class="bi bi-check-lg"></i>
                            <span th:text="${experience.id == null} ? 'Save Entry' : 'Update Entry'">Save</span>
                        </button>
                        <a th:href="@{/admin/experience}" class="btn btn-outline">Cancel</a>
                    </div>
                </form>
            </div>
        </div>
    </div>
</div>

<div id="toastContainer"></div>
<div th:replace="~{fragments/scripts :: scripts}"></div>
</body>
</html>

```

---

## `portfolio-app/src/main/resources/templates/admin/experience-list.html`
<a id="portfolio-app-src-main-resources-templates-admin-experience-listhtml"></a>

```html
<!DOCTYPE html>
<!--
  ============================================================================
  TEMPLATE : admin/experience-list.html   ->  GET /admin/experience
  ============================================================================
-->
<html lang="en" xmlns:th="http://www.thymeleaf.org">
<head th:replace="~{fragments/head :: head('Manage Experience')}"></head>
<body>

<div class="bg-glow"></div>

<div class="admin-shell">
    <aside th:replace="~{fragments/admin-sidebar :: sidebar}"></aside>

    <div class="admin-main">
        <header th:replace="~{fragments/admin-topbar :: topbar('Experience')}"></header>

        <div class="admin-content">
            <div th:replace="~{fragments/alerts :: alerts}"></div>

            <div class="panel">
                <div class="panel-head">
                    <div>
                        <h2>Experience Entries</h2>
                        <p><span th:text="${#lists.size(experiences)}">0</span> record(s)</p>
                    </div>
                    <a th:href="@{/admin/experience/new}" class="btn btn-primary btn-sm">
                        <i class="bi bi-plus-lg"></i> Add Experience
                    </a>
                </div>

                <div class="toolbar">
                    <form th:action="@{/admin/experience}" method="get">
                        <input type="search" name="keyword" class="form-control"
                               placeholder="Search position or organization..." th:value="${keyword}"/>
                        <button type="submit" class="btn btn-ghost btn-sm">
                            <i class="bi bi-search"></i> Search
                        </button>
                        <a th:href="@{/admin/experience}" class="btn btn-outline btn-sm">Reset</a>
                    </form>
                </div>

                <div class="table-wrap" th:unless="${#lists.isEmpty(experiences)}">
                    <table class="data-table">
                        <thead>
                        <tr>
                            <th>Position</th>
                            <th>Organization</th>
                            <th style="width:190px;">Period</th>
                            <th>Technologies</th>
                            <th style="width:130px;">Actions</th>
                        </tr>
                        </thead>
                        <tbody>
                        <tr th:each="exp : ${experiences}">
                            <td>
                                <strong th:text="${exp.position}">Position</strong>
                                <span class="badge badge-success" th:if="${exp.endDate == null}"
                                      style="margin-left:6px;">Current</span>
                            </td>
                            <td th:text="${exp.organization}">Organization</td>
                            <td th:text="${exp.dateRange}">Jun 2025 - Present</td>
                            <td>
                                <span class="text-muted" style="font-size:.84rem;"
                                      th:text="${#strings.abbreviate(exp.technologies, 40)}">Java, Spring</span>
                            </td>
                            <td>
                                <div class="action-row">
                                    <a th:href="@{'/admin/experience/edit/' + ${exp.id}}"
                                       class="btn btn-warning btn-sm" title="Edit">
                                        <i class="bi bi-pencil"></i>
                                    </a>
                                    <form th:action="@{'/admin/experience/delete/' + ${exp.id}}"
                                          method="post"
                                          th:attr="data-confirm='Delete \'' + ${exp.position} + '\'?',
                                                   data-confirm-title='Delete Experience'">
                                        <button type="submit" class="btn btn-danger btn-sm" title="Delete">
                                            <i class="bi bi-trash"></i>
                                        </button>
                                    </form>
                                </div>
                            </td>
                        </tr>
                        </tbody>
                    </table>
                </div>

                <div th:if="${#lists.isEmpty(experiences)}" class="empty-state">
                    <div class="empty-icon"><i class="bi bi-briefcase"></i></div>
                    <p>No experience entries yet.</p>
                </div>
            </div>
        </div>
    </div>
</div>

<div id="toastContainer"></div>
<div th:replace="~{fragments/scripts :: scripts}"></div>
</body>
</html>

```

---

## `portfolio-app/src/main/resources/templates/admin/login.html`
<a id="portfolio-app-src-main-resources-templates-admin-loginhtml"></a>

```html
<!DOCTYPE html>
<!--
  ============================================================================
  TEMPLATE : admin/login.html   ->  GET /admin/login
  ============================================================================
  IMPORTANT: this page only COLLECTS the credentials.
  The <form> posts to /admin/login, which is intercepted by Spring Security
  (see SecurityConfig.formLogin). The controller never sees the password.

  CSRF
    Spring Security requires a CSRF token on every POST. th:action adds it
    automatically as a hidden field - that is why th:action is used instead of
    a plain action attribute.
  ============================================================================
-->
<html lang="en" xmlns:th="http://www.thymeleaf.org">
<head th:replace="~{fragments/head :: head('Admin Login')}"></head>
<body>

<div class="bg-glow"></div>

<div class="login-page">
    <div class="login-card">

        <div class="login-logo"><i class="bi bi-shield-lock-fill"></i></div>
        <h1>Admin Login</h1>
        <p class="login-subtitle">Sign in to manage your portfolio</p>

        <!-- Wrong username / password -->
        <div th:if="${hasError}" class="alert alert-danger">
            <i class="bi bi-exclamation-octagon-fill"></i>
            <span>Invalid username or password. Please try again.</span>
        </div>

        <!-- Just logged out -->
        <div th:if="${hasLogout}" class="alert alert-success">
            <i class="bi bi-check-circle-fill"></i>
            <span>You have been logged out successfully.</span>
        </div>

        <form th:action="@{/admin/login}" method="post">
            <div class="form-group">
                <label class="form-label" for="username">Username</label>
                <input type="text" class="form-control" id="username" name="username"
                       placeholder="Enter your username" required autofocus autocomplete="username"/>
            </div>

            <div class="form-group">
                <label class="form-label" for="password">Password</label>
                <input type="password" class="form-control" id="password" name="password"
                       placeholder="Enter your password" required autocomplete="current-password"/>
            </div>

            <button type="submit" class="btn btn-primary btn-lg btn-block">
                <i class="bi bi-box-arrow-in-right"></i> Sign In
            </button>
        </form>

        <!--
          The default credentials come from application.properties
          (app.security.default-admin-username / default-admin-password).
          Nothing is hard-coded in Java - see DataSeeder.
        -->
        <div class="login-hint">
            <strong>First time here?</strong><br/>
            Default username: <code th:text="${@environment.getProperty('app.security.default-admin-username')}">admin</code><br/>
            Password: the value of <code>app.security.default-admin-password</code>
            (default <code>ChangeMe@123</code>). Change it from
            Settings &rarr; Change Password after your first login.
        </div>

        <a th:href="@{/}" class="login-back">
            <i class="bi bi-arrow-left"></i> Back to portfolio
        </a>
    </div>
</div>

<div id="toastContainer"></div>
<div th:replace="~{fragments/scripts :: scripts}"></div>
</body>
</html>

```

---

## `portfolio-app/src/main/resources/templates/admin/message-list.html`
<a id="portfolio-app-src-main-resources-templates-admin-message-listhtml"></a>

```html
<!DOCTYPE html>
<!--
  ============================================================================
  TEMPLATE : admin/message-list.html   ->  GET /admin/messages
  ============================================================================
  Unread rows are highlighted. Opening a message marks it read automatically.
  ============================================================================
-->
<html lang="en" xmlns:th="http://www.thymeleaf.org">
<head th:replace="~{fragments/head :: head('Messages')}"></head>
<body>

<div class="bg-glow"></div>

<div class="admin-shell">
    <aside th:replace="~{fragments/admin-sidebar :: sidebar}"></aside>

    <div class="admin-main">
        <header th:replace="~{fragments/admin-topbar :: topbar('Messages')}"></header>

        <div class="admin-content">
            <div th:replace="~{fragments/alerts :: alerts}"></div>

            <div class="panel">
                <div class="panel-head">
                    <div>
                        <h2>Contact Messages</h2>
                        <p>
                            <span th:text="${totalCount}">0</span> total,
                            <strong style="color:#ff8b96;" th:text="${unreadCount}">0</strong> unread
                        </p>
                    </div>
                    <div class="gap-row">
                        <a th:href="@{/admin/messages(unreadOnly=true)}"
                           class="btn btn-outline btn-sm" th:classappend="${unreadOnly} ? 'btn-primary'">
                            <i class="bi bi-filter"></i> Unread only
                        </a>
                        <a th:href="@{/admin/messages}" class="btn btn-ghost btn-sm">Show all</a>
                    </div>
                </div>

                <div class="toolbar">
                    <form th:action="@{/admin/messages}" method="get">
                        <input type="search" name="keyword" class="form-control"
                               placeholder="Search name, email, subject..." th:value="${keyword}"/>
                        <button type="submit" class="btn btn-ghost btn-sm">
                            <i class="bi bi-search"></i> Search
                        </button>
                        <a th:href="@{/admin/messages}" class="btn btn-outline btn-sm">Reset</a>
                    </form>

                    <form th:action="@{/admin/messages/delete-all-read}" method="post"
                          data-confirm="Delete every message that is already marked as read? This cannot be undone."
                          data-confirm-title="Delete Read Messages">
                        <button type="submit" class="btn btn-danger btn-sm">
                            <i class="bi bi-trash"></i> Delete all read
                        </button>
                    </form>
                </div>

                <div class="table-wrap" th:unless="${#lists.isEmpty(messages)}">
                    <table class="data-table">
                        <thead>
                        <tr>
                            <th style="width:40px;"></th>
                            <th>Subject</th>
                            <th>From</th>
                            <th style="width:170px;">Received</th>
                            <th style="width:230px;">Actions</th>
                        </tr>
                        </thead>
                        <tbody>
                        <tr th:each="message : ${messages}"
                            th:style="${!message.readStatus} ? 'background:color-mix(in srgb, var(--accent-start) 8%, transparent);'">
                            <td>
                                <span th:if="${!message.readStatus}"
                                      style="color:#ff8b96; font-size:1.1rem;"
                                      title="Unread">&#9679;</span>
                            </td>
                            <td>
                                <a th:href="@{'/admin/messages/view/' + ${message.id}}"
                                   style="color:var(--text-primary); font-weight:600;"
                                   th:text="${message.subject}">Subject</a>
                            </td>
                            <td>
                                <strong th:text="${message.name}">Name</strong>
                                <div class="text-muted" style="font-size:.82rem;"
                                     th:text="${message.email}">email@example.com</div>
                            </td>
                            <td th:text="${#temporals.format(message.createdAt, 'dd MMM yyyy, HH:mm')}">
                                01 Jan 2026, 10:30
                            </td>
                            <td>
                                <div class="action-row">
                                    <a th:href="@{'/admin/messages/view/' + ${message.id}}"
                                       class="btn btn-ghost btn-sm" title="Read">
                                        <i class="bi bi-eye"></i>
                                    </a>

                                    <form th:action="@{'/admin/messages/toggle/' + ${message.id}}"
                                          method="post">
                                        <input type="hidden" name="read"
                                               th:value="${message.readStatus} ? 'false' : 'true'"/>
                                        <button type="submit" class="btn btn-success btn-sm"
                                                th:title="${message.readStatus} ? 'Mark unread' : 'Mark read'">
                                            <i th:class="${message.readStatus}
                                                         ? 'bi bi-envelope-open'
                                                         : 'bi bi-envelope-check'"></i>
                                        </button>
                                    </form>

                                    <form th:action="@{'/admin/messages/delete/' + ${message.id}}"
                                          method="post"
                                          data-confirm="Delete this message permanently?"
                                          data-confirm-title="Delete Message">
                                        <button type="submit" class="btn btn-danger btn-sm" title="Delete">
                                            <i class="bi bi-trash"></i>
                                        </button>
                                    </form>
                                </div>
                            </td>
                        </tr>
                        </tbody>
                    </table>
                </div>

                <div th:if="${#lists.isEmpty(messages)}" class="empty-state">
                    <div class="empty-icon"><i class="bi bi-inbox"></i></div>
                    <p>No messages here yet. Submissions from the contact form appear in this inbox.</p>
                </div>
            </div>
        </div>
    </div>
</div>

<div id="toastContainer"></div>
<div th:replace="~{fragments/scripts :: scripts}"></div>
</body>
</html>

```

---

## `portfolio-app/src/main/resources/templates/admin/message-view.html`
<a id="portfolio-app-src-main-resources-templates-admin-message-viewhtml"></a>

```html
<!DOCTYPE html>
<!--
  ============================================================================
  TEMPLATE : admin/message-view.html   ->  GET /admin/messages/view/{id}
  ============================================================================
  The message body is printed with th:text, which HTML-escapes the content.
  That is what stops a visitor from injecting script through the contact form
  (stored XSS). Never use th:utext for user supplied text.
  ============================================================================
-->
<html lang="en" xmlns:th="http://www.thymeleaf.org">
<head th:replace="~{fragments/head :: head('Message')}"></head>
<body>

<div class="bg-glow"></div>

<div class="admin-shell">
    <aside th:replace="~{fragments/admin-sidebar :: sidebar}"></aside>

    <div class="admin-main">
        <header th:replace="~{fragments/admin-topbar :: topbar('Message')}"></header>

        <div class="admin-content">
            <div th:replace="~{fragments/alerts :: alerts}"></div>

            <div class="panel" style="max-width:860px;">
                <div class="panel-head">
                    <div>
                        <h2 th:text="${message.subject}">Subject</h2>
                        <p>
                            Received
                            <span th:text="${#temporals.format(message.createdAt, 'dd MMM yyyy, HH:mm')}">
                                01 Jan 2026, 10:30
                            </span>
                        </p>
                    </div>
                    <a th:href="@{/admin/messages}" class="btn btn-outline btn-sm">
                        <i class="bi bi-arrow-left"></i> Back to Inbox
                    </a>
                </div>

                <div class="detail-grid mb-3">
                    <div class="detail-block">
                        <h3><i class="bi bi-person"></i> From</h3>
                        <p style="margin:0 0 6px;">
                            <strong style="color:var(--text-primary);" th:text="${message.name}">Name</strong>
                        </p>
                        <a th:href="'mailto:' + ${message.email}" th:text="${message.email}">
                            email@example.com
                        </a>
                    </div>

                    <div class="detail-block">
                        <h3><i class="bi bi-info-circle"></i> Status</h3>
                        <span class="badge badge-success" th:if="${message.readStatus}">Read</span>
                        <span class="badge badge-danger" th:unless="${message.readStatus}">Unread</span>
                        <p style="margin:10px 0 0; font-size:.85rem;" class="text-muted">
                            Message ID: <span th:text="${message.id}">1</span>
                        </p>
                    </div>
                </div>

                <div class="detail-block">
                    <h3><i class="bi bi-chat-left-text"></i> Message</h3>
                    <p style="white-space:pre-wrap; margin:0;" th:text="${message.message}">
                        The message body.
                    </p>
                </div>

                <div class="divider"></div>

                <div class="gap-row">
                    <a th:href="'mailto:' + ${message.email} + '?subject=Re: ' + ${message.subject}"
                       class="btn btn-primary btn-sm">
                        <i class="bi bi-reply-fill"></i> Reply by Email
                    </a>

                    <form th:action="@{'/admin/messages/toggle/' + ${message.id}}" method="post">
                        <input type="hidden" name="read"
                               th:value="${message.readStatus} ? 'false' : 'true'"/>
                        <button type="submit" class="btn btn-success btn-sm">
                            <i class="bi bi-envelope-check"></i>
                            <span th:text="${message.readStatus} ? 'Mark as Unread' : 'Mark as Read'">
                                Mark as Read
                            </span>
                        </button>
                    </form>

                    <form th:action="@{'/admin/messages/delete/' + ${message.id}}" method="post"
                          data-confirm="Delete this message permanently?"
                          data-confirm-title="Delete Message">
                        <button type="submit" class="btn btn-danger btn-sm">
                            <i class="bi bi-trash"></i> Delete
                        </button>
                    </form>
                </div>
            </div>
        </div>
    </div>
</div>

<div id="toastContainer"></div>
<div th:replace="~{fragments/scripts :: scripts}"></div>
</body>
</html>

```

---

## `portfolio-app/src/main/resources/templates/admin/project-form.html`
<a id="portfolio-app-src-main-resources-templates-admin-project-formhtml"></a>

```html
<!DOCTYPE html>
<!--
  ============================================================================
  TEMPLATE : admin/project-form.html
             ->  GET  /admin/projects/new       (create)
             ->  GET  /admin/projects/edit/{id} (update)
             ->  POST /admin/projects/save      (both)
  ============================================================================
  ONE template serves create and edit. The hidden id field decides which one:
  empty id  -> INSERT,  id present -> UPDATE.

  enctype="multipart/form-data" is required because the form can upload an
  image file.

  th:errors prints the message produced by the @NotBlank / @Size annotations
  on the Project entity when the server rejects the submission.
  ============================================================================
-->
<html lang="en" xmlns:th="http://www.thymeleaf.org">
<head th:replace="~{fragments/head :: head(${pageTitle})}"></head>
<body>

<div class="bg-glow"></div>

<div class="admin-shell">
    <aside th:replace="~{fragments/admin-sidebar :: sidebar}"></aside>

    <div class="admin-main">
        <header th:replace="~{fragments/admin-topbar :: topbar(${pageTitle})}"></header>

        <div class="admin-content">
            <div th:replace="~{fragments/alerts :: alerts}"></div>

            <div class="panel">
                <div class="panel-head">
                    <div>
                        <h2 th:text="${pageTitle}">Add New Project</h2>
                        <p>Fields marked <span style="color:#ff6b78;">*</span> are required.</p>
                    </div>
                    <a th:href="@{/admin/projects}" class="btn btn-outline btn-sm">
                        <i class="bi bi-arrow-left"></i> Back to List
                    </a>
                </div>

                <form th:action="@{/admin/projects/save}" th:object="${project}"
                      method="post" enctype="multipart/form-data">

                    <!-- Carries the id on edit, empty on create -->
                    <input type="hidden" th:field="*{id}"/>
                    <input type="hidden" th:field="*{imageUrl}"/>

                    <div class="admin-grid-2">
                        <div>
                            <div class="form-group">
                                <label class="form-label" for="title">
                                    Project Title <span class="req">*</span>
                                </label>
                                <input type="text" class="form-control" id="title"
                                       th:field="*{title}" th:errorclass="is-invalid"
                                       placeholder="Library Management System" maxlength="120" required/>
                                <div class="invalid-feedback" th:if="${#fields.hasErrors('title')}"
                                     th:errors="*{title}">Error</div>
                            </div>

                            <div class="form-group">
                                <label class="form-label" for="description">
                                    Short Description <span class="req">*</span>
                                </label>
                                <textarea class="form-control" id="description"
                                          th:field="*{description}" th:errorclass="is-invalid"
                                          data-maxlength="500"
                                          placeholder="One or two sentences shown on the project card."
                                          required></textarea>
                                <div class="invalid-feedback" th:if="${#fields.hasErrors('description')}"
                                     th:errors="*{description}">Error</div>
                            </div>

                            <div class="form-group">
                                <label class="form-label" for="problemStatement">Problem Statement</label>
                                <textarea class="form-control" id="problemStatement"
                                          th:field="*{problemStatement}" th:errorclass="is-invalid"
                                          data-maxlength="1000"
                                          placeholder="What problem does this project solve?"></textarea>
                                <div class="invalid-feedback"
                                     th:if="${#fields.hasErrors('problemStatement')}"
                                     th:errors="*{problemStatement}">Error</div>
                            </div>

                            <div class="form-group">
                                <label class="form-label" for="features">Features</label>
                                <textarea class="form-control" id="features"
                                          th:field="*{features}" style="min-height:150px;"
                                          placeholder="One feature per line:&#10;Admin and librarian roles&#10;Fine calculation&#10;Search and filter"></textarea>
                                <span class="form-text">One feature per line.</span>
                            </div>
                        </div>

                        <div>
                            <div class="form-group">
                                <label class="form-label" for="technologies">
                                    Technologies <span class="req">*</span>
                                </label>
                                <input type="text" class="form-control" id="technologies"
                                       th:field="*{technologies}" th:errorclass="is-invalid"
                                       placeholder="Java, Spring Boot, MySQL, Bootstrap 5"
                                       maxlength="300" required/>
                                <span class="form-text">Comma separated.</span>
                                <div class="invalid-feedback" th:if="${#fields.hasErrors('technologies')}"
                                     th:errors="*{technologies}">Error</div>
                            </div>

                            <div class="form-row">
                                <div class="form-group">
                                    <label class="form-label" for="category">
                                        Category <span class="req">*</span>
                                    </label>
                                    <select class="form-select" id="category"
                                            th:field="*{category}" th:errorclass="is-invalid">
                                        <option th:each="cat : ${categories}"
                                                th:value="${cat}" th:text="${cat.label}">Java</option>
                                    </select>
                                    <div class="invalid-feedback" th:if="${#fields.hasErrors('category')}"
                                         th:errors="*{category}">Error</div>
                                </div>

                                <div class="form-group">
                                    <label class="form-label" for="sortOrder">Display Order</label>
                                    <input type="number" class="form-control" id="sortOrder"
                                           th:field="*{sortOrder}" min="0" max="999"/>
                                    <span class="form-text">Lower number appears first.</span>
                                </div>
                            </div>

                            <div class="form-group">
                                <label class="form-label" for="githubUrl">GitHub URL</label>
                                <input type="url" class="form-control" id="githubUrl"
                                       th:field="*{githubUrl}" th:errorclass="is-invalid"
                                       placeholder="https://github.com/your-username/project"/>
                                <div class="invalid-feedback" th:if="${#fields.hasErrors('githubUrl')}"
                                     th:errors="*{githubUrl}">Error</div>
                            </div>

                            <div class="form-group">
                                <label class="form-label" for="demoUrl">Live Demo URL</label>
                                <input type="url" class="form-control" id="demoUrl"
                                       th:field="*{demoUrl}" th:errorclass="is-invalid"
                                       placeholder="https://your-demo.example.com"/>
                                <div class="invalid-feedback" th:if="${#fields.hasErrors('demoUrl')}"
                                     th:errors="*{demoUrl}">Error</div>
                            </div>

                            <div class="form-group">
                                <label class="form-label" for="imageFile">Cover Image</label>
                                <input type="file" class="form-control" id="imageFile" name="imageFile"
                                       accept="image/png,image/jpeg,image/webp,image/gif"/>
                                <span class="form-text">
                                    PNG, JPG, WEBP or GIF - maximum 5 MB.
                                </span>
                                <div class="mt-1" th:if="${project.imageUrl}">
                                    <img th:src="${project.imageUrl}" alt="Current cover image"
                                         style="width:150px; border-radius:9px; border:1px solid var(--border-color);"/>
                                    <div class="form-text">Current image - upload a new one to replace it.</div>
                                </div>
                                <div class="invalid-feedback" th:if="${#fields.hasErrors('imageUrl')}"
                                     th:errors="*{imageUrl}">Error</div>
                            </div>

                            <div class="form-group">
                                <label class="form-check">
                                    <input type="checkbox" th:field="*{featured}"/>
                                    <span>Show this project on the public website</span>
                                </label>
                            </div>
                        </div>
                    </div>

                    <div class="divider"></div>

                    <div class="gap-row">
                        <button type="submit" class="btn btn-primary">
                            <i class="bi bi-check-lg"></i>
                            <span th:text="${project.id == null} ? 'Save Project' : 'Update Project'">Save</span>
                        </button>
                        <a th:href="@{/admin/projects}" class="btn btn-outline">Cancel</a>
                    </div>
                </form>
            </div>
        </div>
    </div>
</div>

<div id="toastContainer"></div>
<div th:replace="~{fragments/scripts :: scripts}"></div>
</body>
</html>

```

---

## `portfolio-app/src/main/resources/templates/admin/project-list.html`
<a id="portfolio-app-src-main-resources-templates-admin-project-listhtml"></a>

```html
<!DOCTYPE html>
<!--
  ============================================================================
  TEMPLATE : admin/project-list.html   ->  GET /admin/projects
  ============================================================================
  ============================================================================
-->
<html lang="en" xmlns:th="http://www.thymeleaf.org">
<head th:replace="~{fragments/head :: head('Manage Projects')}"></head>
<body>

<div class="bg-glow"></div>

<div class="admin-shell">
    <aside th:replace="~{fragments/admin-sidebar :: sidebar}"></aside>

    <div class="admin-main">
        <header th:replace="~{fragments/admin-topbar :: topbar('Projects')}"></header>

        <div class="admin-content">
            <div th:replace="~{fragments/alerts :: alerts}"></div>

            <div class="panel">
                <div class="panel-head">
                    <div>
                        <h2>All Projects</h2>
                        <p><span th:text="${#lists.size(projects)}">0</span> project(s) in the database</p>
                    </div>
                    <a th:href="@{/admin/projects/new}" class="btn btn-primary btn-sm">
                        <i class="bi bi-plus-lg"></i> Add Project
                    </a>
                </div>

                <!-- Search + category filter -->
                <div class="toolbar">
                    <form th:action="@{/admin/projects}" method="get">
                        <input type="search" name="keyword" class="form-control"
                               placeholder="Search title, technology..."
                               th:value="${keyword}"/>
                        <button type="submit" class="btn btn-ghost btn-sm">
                            <i class="bi bi-search"></i> Search
                        </button>
                        <a th:href="@{/admin/projects}" class="btn btn-outline btn-sm">Reset</a>
                    </form>

                    <form th:action="@{/admin/projects}" method="get">
                        <select name="category" class="form-select"
                                onchange="this.form.submit()">
                            <option value="">All categories</option>
                            <option th:each="cat : ${categories}"
                                    th:value="${cat}"
                                    th:text="${cat.label}"
                                    th:selected="${selectedCategory != null and selectedCategory == cat}">
                                Java
                            </option>
                        </select>
                    </form>
                </div>

                <!-- Table -->
                <div class="table-wrap" th:unless="${#lists.isEmpty(projects)}">
                    <table class="data-table">
                        <thead>
                        <tr>
                            <th style="width:60px;">Image</th>
                            <th>Title</th>
                            <th>Category</th>
                            <th>Technologies</th>
                            <th style="width:90px;">Visible</th>
                            <th style="width:70px;">Order</th>
                            <th style="width:210px;">Actions</th>
                        </tr>
                        </thead>
                        <tbody>
                        <tr th:each="project : ${projects}">
                            <td>
                                <img th:src="${project.imageUrl} ?: @{/img/project-placeholder.svg}"
                                     th:alt="${project.title}"
                                     style="width:56px; height:36px; object-fit:cover; border-radius:7px;"/>
                            </td>
                            <td><strong th:text="${project.title}">Title</strong></td>
                            <td><span class="badge" th:text="${project.category.label}">Java</span></td>
                            <td>
                                <span class="text-muted" style="font-size:.84rem;"
                                      th:text="${#strings.abbreviate(project.technologies, 46)}">Java, Spring</span>
                            </td>
                            <td>
                                <span class="badge badge-success" th:if="${project.featured}">Yes</span>
                                <span class="badge" th:unless="${project.featured}">No</span>
                            </td>
                            <td th:text="${project.sortOrder}">0</td>
                            <td>
                                <div class="action-row">
                                    <a th:href="@{'/admin/projects/view/' + ${project.id}}"
                                       class="btn btn-ghost btn-sm" title="View">
                                        <i class="bi bi-eye"></i>
                                    </a>
                                    <a th:href="@{'/admin/projects/edit/' + ${project.id}}"
                                       class="btn btn-warning btn-sm" title="Edit">
                                        <i class="bi bi-pencil"></i>
                                    </a>
                                    <form th:action="@{'/admin/projects/delete/' + ${project.id}}"
                                          method="post"
                                          th:attr="data-confirm='Delete the project \'' + ${project.title} + '\'? This cannot be undone.',
                                                   data-confirm-title='Delete Project'">
                                        <button type="submit" class="btn btn-danger btn-sm" title="Delete">
                                            <i class="bi bi-trash"></i>
                                        </button>
                                    </form>
                                </div>
                            </td>
                        </tr>
                        </tbody>
                    </table>
                </div>

                <div th:if="${#lists.isEmpty(projects)}" class="empty-state">
                    <div class="empty-icon"><i class="bi bi-folder2-open"></i></div>
                    <p>No projects found. Add your first project to get started.</p>
                </div>
            </div>
        </div>
    </div>
</div>

<div id="toastContainer"></div>
<div th:replace="~{fragments/scripts :: scripts}"></div>
</body>
</html>

```

---

## `portfolio-app/src/main/resources/templates/admin/settings.html`
<a id="portfolio-app-src-main-resources-templates-admin-settingshtml"></a>

```html
<!DOCTYPE html>
<!--
  ============================================================================
  TEMPLATE : admin/settings.html   ->  GET /admin/settings
  ============================================================================
  Two tabs:
     PROFILE  - every profile field (name, title, intro, social links, services)
     SECURITY - change the login password

  The profile form posts every field under its setting key. The controller
  checks each key against a whitelist before writing it, so no arbitrary row
  can be inserted by adding a field to the HTML.
  ============================================================================
-->
<html lang="en" xmlns:th="http://www.thymeleaf.org">
<head th:replace="~{fragments/head :: head('Settings')}"></head>
<body th:attr="data-tab=${passwordTab} ? 'security' : 'profile'">

<div class="bg-glow"></div>

<div class="admin-shell">
    <aside th:replace="~{fragments/admin-sidebar :: sidebar}"></aside>

    <div class="admin-main">
        <header th:replace="~{fragments/admin-topbar :: topbar('Settings')}"></header>

        <div class="admin-content">
            <div th:replace="~{fragments/alerts :: alerts}"></div>

            <div class="tab-bar">
                <button type="button" class="tab-btn active" data-tab="profile">
                    <i class="bi bi-person-gear"></i> Profile &amp; Content
                </button>
                <button type="button" class="tab-btn" data-tab="security">
                    <i class="bi bi-shield-lock"></i> Security
                </button>
            </div>

            <!-- ==========================================================
                 TAB 1 : PROFILE
                 ========================================================== -->
            <div class="tab-pane active" id="tab-profile">
                <form th:action="@{/admin/settings/save}" method="post"
                      enctype="multipart/form-data">

                    <!-- HERO -->
                    <div class="panel">
                        <div class="panel-head">
                            <div>
                                <h2>Home Page (Hero)</h2>
                                <p>What visitors see first.</p>
                            </div>
                        </div>

                        <div class="form-row">
                            <div class="form-group">
                                <label class="form-label" for="heroName">Full Name</label>
                                <input type="text" class="form-control" id="heroName"
                                       name="hero.name" maxlength="80"
                                       th:value="${settings['hero.name']}"/>
                            </div>
                            <div class="form-group">
                                <label class="form-label" for="heroTitle">Professional Title</label>
                                <input type="text" class="form-control" id="heroTitle"
                                       name="hero.title" maxlength="120"
                                       th:value="${settings['hero.title']}"/>
                            </div>
                        </div>

                        <div class="form-group">
                            <label class="form-label" for="heroIntro">Short Introduction</label>
                            <textarea class="form-control" id="heroIntro" name="hero.intro"
                                      data-maxlength="600"
                                      th:text="${settings['hero.intro']}"></textarea>
                        </div>

                        <div class="form-row">
                            <div class="form-group">
                                <label class="form-label" for="typingWords">Typing Animation Words</label>
                                <input type="text" class="form-control" id="typingWords"
                                       name="hero.typingWords" maxlength="200"
                                       th:value="${settings['hero.typingWords']}"/>
                                <span class="form-text">Comma separated - the hero cycles through them.</span>
                            </div>
                            <div class="form-group">
                                <label class="form-label" for="resumeUrl">Resume URL</label>
                                <input type="text" class="form-control" id="resumeUrl"
                                       name="resume.url" maxlength="200"
                                       th:value="${settings['resume.url']}"/>
                                <span class="form-text">Default is /resume (the PDF inside the app).</span>
                            </div>
                        </div>

                        <div class="form-group">
                            <label class="form-label" for="profileImageFile">Profile Photo</label>
                            <input type="file" class="form-control" id="profileImageFile"
                                   name="profileImageFile"
                                   accept="image/png,image/jpeg,image/webp,image/gif"/>
                            <span class="form-text">PNG, JPG, WEBP or GIF - maximum 5 MB.</span>
                            <div class="mt-1" th:if="${settings['profile.image']}">
                                <img th:src="${settings['profile.image']}" alt="Current profile photo"
                                     style="width:96px; height:96px; object-fit:cover; border-radius:14px;
                                            border:1px solid var(--border-color);"/>
                                <input type="hidden" name="profile.image"
                                       th:value="${settings['profile.image']}"/>
                            </div>
                        </div>
                    </div>

                    <!-- ABOUT -->
                    <div class="panel">
                        <div class="panel-head">
                            <div>
                                <h2>About Me</h2>
                                <p>The text and details on the About page.</p>
                            </div>
                        </div>

                        <div class="form-group">
                            <label class="form-label" for="aboutIntro">Introduction Paragraph</label>
                            <textarea class="form-control" id="aboutIntro" name="about.intro"
                                      data-maxlength="900"
                                      th:text="${settings['about.intro']}"></textarea>
                        </div>

                        <div class="form-group">
                            <label class="form-label" for="aboutObjective">Career Objective</label>
                            <textarea class="form-control" id="aboutObjective" name="about.objective"
                                      data-maxlength="600"
                                      th:text="${settings['about.objective']}"></textarea>
                        </div>

                        <div class="form-row">
                            <div class="form-group">
                                <label class="form-label" for="aboutInterests">Interests</label>
                                <input type="text" class="form-control" id="aboutInterests"
                                       name="about.interests" maxlength="200"
                                       th:value="${settings['about.interests']}"/>
                                <span class="form-text">Comma separated.</span>
                            </div>
                            <div class="form-group">
                                <label class="form-label" for="aboutLanguages">Languages</label>
                                <input type="text" class="form-control" id="aboutLanguages"
                                       name="about.languages" maxlength="120"
                                       th:value="${settings['about.languages']}"/>
                                <span class="form-text">Comma separated.</span>
                            </div>
                        </div>

                        <div class="form-row">
                            <div class="form-group">
                                <label class="form-label" for="aboutDob">Date of Birth</label>
                                <input type="text" class="form-control" id="aboutDob"
                                       name="about.dob" maxlength="30"
                                       th:value="${settings['about.dob']}"/>
                            </div>
                            <div class="form-group">
                                <label class="form-label" for="aboutEmail">Email</label>
                                <input type="email" class="form-control" id="aboutEmail"
                                       name="about.email" maxlength="120"
                                       th:value="${settings['about.email']}"/>
                            </div>
                        </div>

                        <div class="form-row">
                            <div class="form-group">
                                <label class="form-label" for="aboutPhone">Phone</label>
                                <input type="text" class="form-control" id="aboutPhone"
                                       name="about.phone" maxlength="30"
                                       th:value="${settings['about.phone']}"/>
                            </div>
                            <div class="form-group">
                                <label class="form-label" for="aboutLocation">Location</label>
                                <input type="text" class="form-control" id="aboutLocation"
                                       name="about.location" maxlength="80"
                                       th:value="${settings['about.location']}"/>
                            </div>
                        </div>
                    </div>

                    <!-- SOCIAL -->
                    <div class="panel">
                        <div class="panel-head">
                            <div>
                                <h2>Social Links</h2>
                                <p>Leave a field empty to hide that button everywhere on the site.</p>
                            </div>
                        </div>

                        <div class="form-row">
                            <div class="form-group">
                                <label class="form-label" for="socialGithub">GitHub</label>
                                <input type="url" class="form-control" id="socialGithub"
                                       name="social.github" maxlength="200"
                                       th:value="${settings['social.github']}"/>
                            </div>
                            <div class="form-group">
                                <label class="form-label" for="socialLinkedin">LinkedIn</label>
                                <input type="url" class="form-control" id="socialLinkedin"
                                       name="social.linkedin" maxlength="200"
                                       th:value="${settings['social.linkedin']}"/>
                            </div>
                        </div>

                        <div class="form-row">
                            <div class="form-group">
                                <label class="form-label" for="socialTwitter">Twitter / X</label>
                                <input type="url" class="form-control" id="socialTwitter"
                                       name="social.twitter" maxlength="200"
                                       th:value="${settings['social.twitter']}"/>
                            </div>
                            <div class="form-group">
                                <label class="form-label" for="socialInstagram">Instagram</label>
                                <input type="url" class="form-control" id="socialInstagram"
                                       name="social.instagram" maxlength="200"
                                       th:value="${settings['social.instagram']}"/>
                            </div>
                        </div>
                    </div>

                    <!-- SERVICES -->
                    <div class="panel">
                        <div class="panel-head">
                            <div>
                                <h2>Services ("What I Do")</h2>
                                <p>One card per line.</p>
                            </div>
                        </div>

                        <div class="form-group">
                            <label class="form-label" for="servicesList">Service List</label>
                            <textarea class="form-control" id="servicesList" name="services.list"
                                      style="min-height:170px; font-family:monospace; font-size:.86rem;"
                                      th:text="${settings['services.list']}"></textarea>
                            <span class="form-text">
                                Format per line: <code>icon|title|description</code>
                                - for example <code>code|Java Development|Building Spring Boot applications</code>.
                                Icon names are Bootstrap Icons (code, globe, database, robot, gear, brush...).
                            </span>
                        </div>
                    </div>

                    <div class="panel">
                        <div class="gap-row">
                            <button type="submit" class="btn btn-primary btn-lg">
                                <i class="bi bi-check-lg"></i> Save All Changes
                            </button>
                            <a th:href="@{/}" target="_blank" class="btn btn-outline">
                                <i class="bi bi-globe2"></i> Preview Website
                            </a>
                        </div>
                    </div>
                </form>
            </div>

            <!-- ==========================================================
                 TAB 2 : SECURITY
                 ========================================================== -->
            <div class="tab-pane" id="tab-security">
                <div class="panel" style="max-width:620px;">
                    <div class="panel-head">
                        <div>
                            <h2>Change Password</h2>
                            <p>
                                Your password is stored as a BCrypt hash, so it can never be read
                                back - not even by you. If you forget it, set
                                <code>app.security.default-admin-password</code> and clear the
                                admin_users table to re-seed.
                            </p>
                        </div>
                    </div>

                    <form th:action="@{/admin/settings/change-password}"
                          th:object="${changePasswordForm}" method="post">

                        <div class="form-group">
                            <label class="form-label" for="currentPassword">
                                Current Password <span class="req">*</span>
                            </label>
                            <input type="password" class="form-control" id="currentPassword"
                                   th:field="*{currentPassword}" th:errorclass="is-invalid"
                                   autocomplete="current-password" required/>
                            <div class="invalid-feedback"
                                 th:if="${#fields.hasErrors('currentPassword')}"
                                 th:errors="*{currentPassword}">Error</div>
                        </div>

                        <div class="form-group">
                            <label class="form-label" for="newPassword">
                                New Password <span class="req">*</span>
                            </label>
                            <input type="password" class="form-control" id="newPassword"
                                   th:field="*{newPassword}" th:errorclass="is-invalid"
                                   minlength="8" autocomplete="new-password" required/>
                            <span class="form-text">At least 8 characters.</span>
                            <div class="invalid-feedback" th:if="${#fields.hasErrors('newPassword')}"
                                 th:errors="*{newPassword}">Error</div>
                        </div>

                        <div class="form-group">
                            <label class="form-label" for="confirmPassword">
                                Confirm New Password <span class="req">*</span>
                            </label>
                            <input type="password" class="form-control" id="confirmPassword"
                                   th:field="*{confirmPassword}" th:errorclass="is-invalid"
                                   autocomplete="new-password" required/>
                            <div class="invalid-feedback"
                                 th:if="${#fields.hasErrors('confirmPassword')}"
                                 th:errors="*{confirmPassword}">Error</div>
                            <div class="invalid-feedback"
                                 th:if="${#fields.hasErrors('passwordMatching')}"
                                 th:errors="*{passwordMatching}">Error</div>
                        </div>

                        <div class="divider"></div>

                        <button type="submit" class="btn btn-primary">
                            <i class="bi bi-key-fill"></i> Update Password
                        </button>
                    </form>
                </div>

                <div class="panel" style="max-width:620px;">
                    <div class="panel-head">
                        <div>
                            <h2>Where Credentials Come From</h2>
                            <p>No password exists anywhere in the Java source code.</p>
                        </div>
                    </div>
                    <ul class="bullet-list">
                        <li>The first account is created by <strong>DataSeeder</strong> on the first start.</li>
                        <li>
                            Username: <code th:text="${@environment.getProperty('app.security.default-admin-username')}">
                            admin</code>
                        </li>
                        <li>
                            Password: the value of <code>app.security.default-admin-password</code>,
                            overridable with the <code>ADMIN_PASSWORD</code> environment variable.
                        </li>
                        <li>Only a BCrypt hash of it is written to the <code>admin_users</code> table.</li>
                        <li>Use the form above to change it at any time.</li>
                    </ul>
                </div>
            </div>
        </div>
    </div>
</div>

<div id="toastContainer"></div>
<div th:replace="~{fragments/scripts :: scripts}"></div>
</body>
</html>

```

---

## `portfolio-app/src/main/resources/templates/admin/skill-form.html`
<a id="portfolio-app-src-main-resources-templates-admin-skill-formhtml"></a>

```html
<!DOCTYPE html>
<!--
  ============================================================================
  TEMPLATE : admin/skill-form.html
             ->  GET  /admin/skills/new
             ->  GET  /admin/skills/edit/{id}
             ->  POST /admin/skills/save
  ============================================================================
  The range slider is paired with a numeric output that js/app.js keeps in
  sync (see initRangeLabels). A datalist suggests categories already used,
  while still allowing a brand new category to be typed.
  ============================================================================
-->
<html lang="en" xmlns:th="http://www.thymeleaf.org">
<head th:replace="~{fragments/head :: head(${pageTitle})}"></head>
<body>

<div class="bg-glow"></div>

<div class="admin-shell">
    <aside th:replace="~{fragments/admin-sidebar :: sidebar}"></aside>

    <div class="admin-main">
        <header th:replace="~{fragments/admin-topbar :: topbar(${pageTitle})}"></header>

        <div class="admin-content">
            <div th:replace="~{fragments/alerts :: alerts}"></div>

            <div class="panel" style="max-width:720px;">
                <div class="panel-head">
                    <div>
                        <h2 th:text="${pageTitle}">Add New Skill</h2>
                        <p>Skills are grouped by category on the public page.</p>
                    </div>
                    <a th:href="@{/admin/skills}" class="btn btn-outline btn-sm">
                        <i class="bi bi-arrow-left"></i> Back to List
                    </a>
                </div>

                <form th:action="@{/admin/skills/save}" th:object="${skill}" method="post">
                    <input type="hidden" th:field="*{id}"/>

                    <div class="form-group">
                        <label class="form-label" for="name">
                            Skill Name <span class="req">*</span>
                        </label>
                        <input type="text" class="form-control" id="name"
                               th:field="*{name}" th:errorclass="is-invalid"
                               placeholder="Spring Boot" maxlength="60" required/>
                        <div class="invalid-feedback" th:if="${#fields.hasErrors('name')}"
                             th:errors="*{name}">Error</div>
                    </div>

                    <div class="form-group">
                        <label class="form-label" for="category">
                            Category <span class="req">*</span>
                        </label>
                        <input type="text" class="form-control" id="category" list="categoryOptions"
                               th:field="*{category}" th:errorclass="is-invalid"
                               placeholder="Programming Languages" maxlength="60" required/>
                        <datalist id="categoryOptions">
                            <option th:each="existing : ${existingCategories}" th:value="${existing}"></option>
                            <option value="Programming Languages"></option>
                            <option value="Web Technologies"></option>
                            <option value="Backend"></option>
                            <option value="Database"></option>
                            <option value="Tools"></option>
                            <option value="Other Technologies"></option>
                        </datalist>
                        <span class="form-text">Pick an existing category or type a new one.</span>
                        <div class="invalid-feedback" th:if="${#fields.hasErrors('category')}"
                             th:errors="*{category}">Error</div>
                    </div>

                    <div class="form-group">
                        <label class="form-label" for="proficiency">
                            Proficiency <span class="req">*</span>
                        </label>
                        <div class="gap-row">
                            <input type="range" class="form-range" id="proficiencyRange"
                                   min="0" max="100" step="5"
                                   th:value="${skill.proficiency}"
                                   data-output="proficiencyOutput"
                                   style="flex:1 1 220px;"/>
                            <strong id="proficiencyOutput"
                                    style="min-width:52px; color:var(--accent-solid);">75%</strong>
                        </div>
                        <!-- The real submitted field; the slider writes into it -->
                        <input type="number" class="form-control mt-1" id="proficiency"
                               th:field="*{proficiency}" th:errorclass="is-invalid"
                               min="0" max="100" required/>
                        <div class="invalid-feedback" th:if="${#fields.hasErrors('proficiency')}"
                             th:errors="*{proficiency}">Error</div>
                        <span class="form-text">
                            0 - 100. This value sets the width of the progress bar.
                        </span>
                    </div>

                    <div class="form-group">
                        <label class="form-label" for="sortOrder">Display Order</label>
                        <input type="number" class="form-control" id="sortOrder"
                               th:field="*{sortOrder}" min="0" max="999"/>
                        <span class="form-text">Lower number appears first inside the category.</span>
                    </div>

                    <div class="divider"></div>

                    <div class="gap-row">
                        <button type="submit" class="btn btn-primary">
                            <i class="bi bi-check-lg"></i>
                            <span th:text="${skill.id == null} ? 'Save Skill' : 'Update Skill'">Save</span>
                        </button>
                        <a th:href="@{/admin/skills}" class="btn btn-outline">Cancel</a>
                    </div>
                </form>
            </div>
        </div>
    </div>
</div>

<!-- Keep the slider and the number field in sync -->
<script>
    document.addEventListener('DOMContentLoaded', function () {
        var range = document.getElementById('proficiencyRange');
        var number = document.getElementById('proficiency');
        var output = document.getElementById('proficiencyOutput');
        if (!range || !number) return;

        function syncFromRange() {
            number.value = range.value;
            if (output) output.textContent = range.value + '%';
        }

        function syncFromNumber() {
            var value = Math.max(0, Math.min(100, parseInt(number.value, 10) || 0));
            range.value = value;
            if (output) output.textContent = value + '%';
        }

        range.addEventListener('input', syncFromRange);
        number.addEventListener('input', syncFromNumber);
        syncFromNumber();
    });
</script>

<div id="toastContainer"></div>
<div th:replace="~{fragments/scripts :: scripts}"></div>
</body>
</html>

```

---

## `portfolio-app/src/main/resources/templates/admin/skill-list.html`
<a id="portfolio-app-src-main-resources-templates-admin-skill-listhtml"></a>

```html
<!DOCTYPE html>
<!--
  ============================================================================
  TEMPLATE : admin/skill-list.html   ->  GET /admin/skills
  ============================================================================
-->
<html lang="en" xmlns:th="http://www.thymeleaf.org">
<head th:replace="~{fragments/head :: head('Manage Skills')}"></head>
<body>

<div class="bg-glow"></div>

<div class="admin-shell">
    <aside th:replace="~{fragments/admin-sidebar :: sidebar}"></aside>

    <div class="admin-main">
        <header th:replace="~{fragments/admin-topbar :: topbar('Skills')}"></header>

        <div class="admin-content">
            <div th:replace="~{fragments/alerts :: alerts}"></div>

            <div class="panel">
                <div class="panel-head">
                    <div>
                        <h2>All Skills</h2>
                        <p><span th:text="${totalSkills}">0</span> skill(s) in the database</p>
                    </div>
                    <a th:href="@{/admin/skills/new}" class="btn btn-primary btn-sm">
                        <i class="bi bi-plus-lg"></i> Add Skill
                    </a>
                </div>

                <div class="toolbar">
                    <form th:action="@{/admin/skills}" method="get">
                        <input type="search" name="keyword" class="form-control"
                               placeholder="Search skill or category..." th:value="${keyword}"/>
                        <button type="submit" class="btn btn-ghost btn-sm">
                            <i class="bi bi-search"></i> Search
                        </button>
                        <a th:href="@{/admin/skills}" class="btn btn-outline btn-sm">Reset</a>
                    </form>
                </div>

                <div class="table-wrap" th:unless="${#lists.isEmpty(skills)}">
                    <table class="data-table">
                        <thead>
                        <tr>
                            <th>Skill</th>
                            <th>Category</th>
                            <th style="width:240px;">Proficiency</th>
                            <th style="width:70px;">Order</th>
                            <th style="width:130px;">Actions</th>
                        </tr>
                        </thead>
                        <tbody>
                        <tr th:each="skill : ${skills}">
                            <td><strong th:text="${skill.name}">Java</strong></td>
                            <td><span class="badge badge-soft" th:text="${skill.category}">Languages</span></td>
                            <td>
                                <div class="skill-head" style="margin-bottom:4px;">
                                    <span class="skill-pct" th:text="${skill.proficiency} + '%'">90%</span>
                                </div>
                                <div class="progress-track">
                                    <div class="progress-fill"
                                         th:classappend="${skill.barClass}"
                                         th:style="'width:' + ${skill.proficiency} + '%'"></div>
                                </div>
                            </td>
                            <td th:text="${skill.sortOrder}">0</td>
                            <td>
                                <div class="action-row">
                                    <a th:href="@{'/admin/skills/edit/' + ${skill.id}}"
                                       class="btn btn-warning btn-sm" title="Edit">
                                        <i class="bi bi-pencil"></i>
                                    </a>
                                    <form th:action="@{'/admin/skills/delete/' + ${skill.id}}"
                                          method="post"
                                          th:attr="data-confirm='Delete the skill \'' + ${skill.name} + '\'?',
                                                   data-confirm-title='Delete Skill'">
                                        <button type="submit" class="btn btn-danger btn-sm" title="Delete">
                                            <i class="bi bi-trash"></i>
                                        </button>
                                    </form>
                                </div>
                            </td>
                        </tr>
                        </tbody>
                    </table>
                </div>

                <div th:if="${#lists.isEmpty(skills)}" class="empty-state">
                    <div class="empty-icon"><i class="bi bi-bar-chart"></i></div>
                    <p>No skills found. Add the technologies you work with.</p>
                </div>
            </div>
        </div>
    </div>
</div>

<div id="toastContainer"></div>
<div th:replace="~{fragments/scripts :: scripts}"></div>
</body>
</html>

```

---

# 14. Error Page Templates

## `portfolio-app/src/main/resources/templates/error/404.html`
<a id="portfolio-app-src-main-resources-templates-error-404html"></a>

```html
<!DOCTYPE html>
<!--
  ============================================================================
  TEMPLATE : error/404.html
  ============================================================================
  Spring Boot automatically renders templates/error/<status>.html for container
  level errors that never reach a controller (for example a URL that no
  @RequestMapping matches).
  ============================================================================
-->
<html lang="en" xmlns:th="http://www.thymeleaf.org">
<head th:replace="~{fragments/head :: head('404 - Page Not Found')}"></head>
<body>

<div class="bg-glow"></div>
<nav th:replace="~{fragments/navbar :: navbar}"></nav>

<main>
    <section class="section" style="min-height:70vh; display:grid; place-items:center;">
        <div class="container-px">
            <div class="card-glass text-center reveal visible"
                 style="max-width:620px; margin:0 auto; padding:48px 30px;">
                <div style="font-size:5.2rem; font-weight:800; line-height:1;
                            background:var(--gradient); -webkit-background-clip:text;
                            background-clip:text; color:transparent;">404</div>
                <h1 style="font-size:1.7rem; margin-top:12px;">Page Not Found</h1>
                <p>
                    The page you are looking for does not exist, has been moved,
                    or the link is broken.
                </p>
                <p class="text-muted" style="font-size:.84rem;" th:if="${path}">
                    Requested: <code th:text="${path}">/unknown</code>
                </p>
                <div class="gap-row" style="justify-content:center; margin-top:22px;">
                    <a th:href="@{/}" class="btn btn-primary">
                        <i class="bi bi-house-door-fill"></i> Go to Home
                    </a>
                    <a th:href="@{/projects}" class="btn btn-outline">
                        <i class="bi bi-collection"></i> Browse Projects
                    </a>
                </div>
            </div>
        </div>
    </section>
</main>

<footer th:replace="~{fragments/footer :: footer}"></footer>
<div id="toastContainer"></div>
<div th:replace="~{fragments/scripts :: scripts}"></div>
</body>
</html>

```

---

## `portfolio-app/src/main/resources/templates/error/500.html`
<a id="portfolio-app-src-main-resources-templates-error-500html"></a>

```html
<!DOCTYPE html>
<!--
  ============================================================================
  TEMPLATE : error/500.html   (server error)
  ============================================================================
  Shown when something unexpected goes wrong. The real cause is in the server
  console log - it is deliberately NOT shown to the visitor, because stack
  traces leak implementation details.
  ============================================================================
-->
<html lang="en" xmlns:th="http://www.thymeleaf.org">
<head th:replace="~{fragments/head :: head('500 - Server Error')}"></head>
<body>

<div class="bg-glow"></div>
<nav th:replace="~{fragments/navbar :: navbar}"></nav>

<main>
    <section class="section" style="min-height:70vh; display:grid; place-items:center;">
        <div class="container-px">
            <div class="card-glass text-center reveal visible"
                 style="max-width:620px; margin:0 auto; padding:48px 30px;">
                <div style="font-size:5.2rem; font-weight:800; line-height:1;
                            background:var(--gradient); -webkit-background-clip:text;
                            background-clip:text; color:transparent;">500</div>
                <h1 style="font-size:1.7rem; margin-top:12px;">Something Went Wrong</h1>
                <p>
                    An unexpected error occurred on the server. Please try again in a
                    moment, or go back to the home page.
                </p>
                <p class="text-muted" style="font-size:.84rem;">
                    If this keeps happening, check the application console for the details.
                </p>
                <div class="gap-row" style="justify-content:center; margin-top:22px;">
                    <a th:href="@{/}" class="btn btn-primary">
                        <i class="bi bi-house-door-fill"></i> Go to Home
                    </a>
                    <a th:href="@{/contact}" class="btn btn-outline">
                        <i class="bi bi-envelope"></i> Contact Me
                    </a>
                </div>
            </div>
        </div>
    </section>
</main>

<footer th:replace="~{fragments/footer :: footer}"></footer>
<div id="toastContainer"></div>
<div th:replace="~{fragments/scripts :: scripts}"></div>
</body>
</html>

```

---

## `portfolio-app/src/main/resources/templates/error/access-denied.html`
<a id="portfolio-app-src-main-resources-templates-error-access-deniedhtml"></a>

```html
<!DOCTYPE html>
<!--
  ============================================================================
  TEMPLATE : error/access-denied.html   (403)
  ============================================================================
  Configured in SecurityConfig as the accessDeniedPage. It is shown to a user
  who IS logged in but does not have the required role.
  (An anonymous visitor is sent to the login page instead, which is the
  standard Spring Security behaviour.)
  ============================================================================
-->
<html lang="en" xmlns:th="http://www.thymeleaf.org">
<head th:replace="~{fragments/head :: head('403 - Access Denied')}"></head>
<body>

<div class="bg-glow"></div>
<nav th:replace="~{fragments/navbar :: navbar}"></nav>

<main>
    <section class="section" style="min-height:70vh; display:grid; place-items:center;">
        <div class="container-px">
            <div class="card-glass text-center reveal visible"
                 style="max-width:620px; margin:0 auto; padding:48px 30px;">
                <div class="service-icon" style="margin:0 auto 18px; width:74px; height:74px;
                            font-size:2rem; background:rgba(220,53,69,.15); color:#ff8b96;">
                    <i class="bi bi-shield-lock-fill"></i>
                </div>

                <div style="font-size:3.4rem; font-weight:800; line-height:1;
                            background:var(--gradient); -webkit-background-clip:text;
                            background-clip:text; color:transparent;">403</div>

                <h1 style="font-size:1.7rem; margin-top:12px;">Access Denied</h1>
                <p>
                    You do not have permission to open this page. The admin area is
                    restricted to accounts with the ADMIN role.
                </p>

                <div class="gap-row" style="justify-content:center; margin-top:22px;">
                    <a th:href="@{/}" class="btn btn-primary">
                        <i class="bi bi-house-door-fill"></i> Go to Home
                    </a>
                    <a th:href="@{/admin/login}" class="btn btn-outline">
                        <i class="bi bi-box-arrow-in-right"></i> Admin Login
                    </a>
                </div>
            </div>
        </div>
    </section>
</main>

<footer th:replace="~{fragments/footer :: footer}"></footer>
<div id="toastContainer"></div>
<div th:replace="~{fragments/scripts :: scripts}"></div>
</body>
</html>

```

---

## `portfolio-app/src/main/resources/templates/error/error.html`
<a id="portfolio-app-src-main-resources-templates-error-errorhtml"></a>

```html
<!DOCTYPE html>
<!--
  ============================================================================
  TEMPLATE : error/error.html
  ============================================================================
  Used by GlobalExceptionHandler for 400 / 404 / 500.
  Spring Boot also falls back to templates/error/404.html and 500.html (see
  those files) when a container-level error occurs outside a controller.

  WHAT THE VISITOR SEES
    - a status code
    - a friendly heading
    - a short explanation
    - buttons to go home or back

  WHAT THE VISITOR NEVER SEES
    - the stack trace (it is written to the server log instead)
  ============================================================================
-->
<html lang="en" xmlns:th="http://www.thymeleaf.org">
<head th:replace="~{fragments/head :: head('Error')}"></head>
<body>

<div class="bg-glow"></div>
<nav th:replace="~{fragments/navbar :: navbar}"></nav>

<main>
    <section class="section" style="min-height:70vh; display:grid; place-items:center;">
        <div class="container-px">
            <div class="card-glass text-center reveal visible"
                 style="max-width:620px; margin:0 auto; padding:48px 30px;">

                <div style="font-size:5.2rem; font-weight:800; line-height:1;
                            background:var(--gradient); -webkit-background-clip:text;
                            background-clip:text; color:transparent;"
                     th:text="${status} ?: '404'">404</div>

                <h1 style="font-size:1.7rem; margin-top:12px;"
                    th:text="${title} ?: 'Page Not Found'">Page Not Found</h1>

                <p th:text="${message} ?: 'The page you are looking for does not exist.'">
                    The page you are looking for does not exist.
                </p>

                <p class="text-muted" style="font-size:.84rem;" th:if="${path}">
                    Requested: <code th:text="${path}">/unknown</code>
                </p>

                <div class="gap-row" style="justify-content:center; margin-top:22px;">
                    <a th:href="@{/}" class="btn btn-primary">
                        <i class="bi bi-house-door-fill"></i> Go to Home
                    </a>
                    <a th:href="@{/projects}" class="btn btn-outline">
                        <i class="bi bi-collection"></i> Browse Projects
                    </a>
                </div>
            </div>
        </div>
    </section>
</main>

<footer th:replace="~{fragments/footer :: footer}"></footer>
<div id="toastContainer"></div>
<div th:replace="~{fragments/scripts :: scripts}"></div>
</body>
</html>

```

---

# 15. Styles & Scripts

## `portfolio-app/src/main/resources/static/css/style.css`
<a id="portfolio-app-src-main-resources-static-css-stylecss"></a>

```css
/* ==========================================================================
   PERSONAL PORTFOLIO - MAIN STYLESHEET
   ==========================================================================
   This file is written so the site looks correct on its own, and Bootstrap 5
   (loaded from the CDN in the HTML) only adds polish on top.

   HOW DARK / LIGHT MODE WORKS
     :root                     -> dark theme variables (the default)
     html[data-theme="light"]  -> the same variable names, light values
     Every rule below uses var(--...), so switching the attribute on <html>
     re-themes the whole site instantly. JavaScript toggles that attribute
     and remembers the choice in localStorage.
   ========================================================================== */

/* ==========================================================================
   1. THEME VARIABLES
   ========================================================================== */
:root {
    /* Core colours - DARK (default) */
    --bg-primary: #0a0e17;
    --bg-secondary: #111725;
    --bg-card: rgba(255, 255, 255, 0.045);
    --bg-card-hover: rgba(255, 255, 255, 0.075);
    --border-color: rgba(255, 255, 255, 0.10);
    --text-primary: #eef2f8;
    --text-secondary: #a4b0c4;
    --text-muted: #7c879b;

    /* Brand gradient */
    --accent-start: #4f7cff;
    --accent-end: #9b5cff;
    --accent-solid: #6d8dff;
    --gradient: linear-gradient(135deg, #4f7cff 0%, #9b5cff 100%);

    /* Effects */
    --shadow-soft: 0 10px 30px rgba(0, 0, 0, 0.35);
    --shadow-lift: 0 18px 45px rgba(0, 0, 0, 0.45);
    --glow: 0 0 0 1px rgba(255, 255, 255, 0.06), 0 12px 40px rgba(79, 124, 255, 0.18);

    /* Sizes */
    --radius: 16px;
    --radius-sm: 10px;
    --navbar-height: 72px;
}

html[data-theme="light"] {
    --bg-primary: #f5f7fb;
    --bg-secondary: #ffffff;
    --bg-card: rgba(255, 255, 255, 0.85);
    --bg-card-hover: #ffffff;
    --border-color: rgba(15, 23, 42, 0.10);
    --text-primary: #101828;
    --text-secondary: #475467;
    --text-muted: #6b7688;

    --accent-start: #3b63e0;
    --accent-end: #8b3ff0;
    --accent-solid: #4a6ee0;
    --gradient: linear-gradient(135deg, #3b63e0 0%, #8b3ff0 100%);

    --shadow-soft: 0 10px 30px rgba(16, 24, 40, 0.08);
    --shadow-lift: 0 18px 45px rgba(16, 24, 40, 0.14);
    --glow: 0 0 0 1px rgba(59, 99, 224, 0.10), 0 12px 40px rgba(59, 99, 224, 0.14);
}

/* ==========================================================================
   2. BASE / RESET
   ========================================================================== */
* {
    box-sizing: border-box;
}

html {
    scroll-behavior: smooth;          /* smooth scrolling for the anchor links */
    scroll-padding-top: calc(var(--navbar-height) + 16px);
}

body {
    margin: 0;
    font-family: "Inter", "Segoe UI", system-ui, -apple-system, "Helvetica Neue", Arial, sans-serif;
    background-color: var(--bg-primary);
    color: var(--text-primary);
    line-height: 1.65;
    -webkit-font-smoothing: antialiased;
    transition: background-color .35s ease, color .35s ease;
    overflow-x: hidden;
}

h1, h2, h3, h4, h5, h6 {
    color: var(--text-primary);
    font-weight: 700;
    line-height: 1.25;
    margin: 0 0 .6rem;
}

h1 { font-size: clamp(2.1rem, 5vw, 3.4rem); }
h2 { font-size: clamp(1.6rem, 3.4vw, 2.3rem); }
h3 { font-size: clamp(1.15rem, 2.2vw, 1.4rem); }

p {
    color: var(--text-secondary);
    margin: 0 0 1rem;
}

a {
    color: var(--accent-solid);
    text-decoration: none;
    transition: color .2s ease, opacity .2s ease;
}

a:hover { color: var(--accent-end); }

img { max-width: 100%; height: auto; display: block; }

/* ==========================================================================
   3. LAYOUT (small grid system, independent of Bootstrap)
   ========================================================================== */
.container-px {
    width: 100%;
    max-width: 1180px;
    margin: 0 auto;
    padding: 0 20px;
}

.row-grid {
    display: flex;
    flex-wrap: wrap;
    margin: 0 -12px;
}

.col {
    padding: 0 12px;
    flex: 1 1 0;
    min-width: 0;
}

/* Responsive column widths: col-6 = half, col-4 = third, col-3 = quarter */
.col-12 { flex: 0 0 100%; max-width: 100%; }
.col-6  { flex: 0 0 50%;  max-width: 50%; }
.col-4  { flex: 0 0 33.3333%; max-width: 33.3333%; }
.col-3  { flex: 0 0 25%;  max-width: 25%; }

@media (max-width: 991px) {
    .col-4, .col-3 { flex: 0 0 50%; max-width: 50%; }
}

@media (max-width: 640px) {
    .col-6, .col-4, .col-3 { flex: 0 0 100%; max-width: 100%; }
}

.section {
    padding: 84px 0;
    position: relative;
}

.section-tight { padding: 56px 0; }

.section-alt { background-color: var(--bg-secondary); }

/* Section heading block used on every page */
.section-heading {
    text-align: center;
    max-width: 720px;
    margin: 0 auto 46px;
}

.section-heading .eyebrow {
    display: inline-block;
    font-size: .78rem;
    font-weight: 700;
    letter-spacing: .16em;
    text-transform: uppercase;
    background: var(--gradient);
    -webkit-background-clip: text;
    background-clip: text;
    color: transparent;
    margin-bottom: 10px;
}

.section-heading p { color: var(--text-muted); margin-bottom: 0; }

/* ==========================================================================
   4. BACKGROUND DECORATION (subtle animated glow)
   ========================================================================== */
.bg-glow {
    position: fixed;
    inset: 0;
    z-index: -1;
    overflow: hidden;
    pointer-events: none;
}

.bg-glow::before,
.bg-glow::after {
    content: "";
    position: absolute;
    width: 46vw;
    height: 46vw;
    border-radius: 50%;
    filter: blur(110px);
    opacity: .30;
    animation: floatBlob 22s ease-in-out infinite alternate;
}

.bg-glow::before {
    background: var(--accent-start);
    top: -14vw;
    left: -10vw;
}

.bg-glow::after {
    background: var(--accent-end);
    bottom: -16vw;
    right: -12vw;
    animation-delay: -11s;
}

html[data-theme="light"] .bg-glow::before,
html[data-theme="light"] .bg-glow::after { opacity: .16; }

@keyframes floatBlob {
    0%   { transform: translate3d(0, 0, 0) scale(1); }
    100% { transform: translate3d(4vw, 5vh, 0) scale(1.12); }
}

/* Respects the OS "reduce motion" setting */
@media (prefers-reduced-motion: reduce) {
    *, *::before, *::after {
        animation-duration: .001ms !important;
        animation-iteration-count: 1 !important;
        transition-duration: .001ms !important;
        scroll-behavior: auto !important;
    }
}

/* ==========================================================================
   5. NAVBAR (sticky, glass)
   ========================================================================== */
.site-navbar {
    position: sticky;
    top: 0;
    z-index: 1030;
    height: var(--navbar-height);
    display: flex;
    align-items: center;
    background: color-mix(in srgb, var(--bg-primary) 78%, transparent);
    backdrop-filter: blur(14px);
    -webkit-backdrop-filter: blur(14px);
    border-bottom: 1px solid var(--border-color);
    transition: box-shadow .3s ease, background-color .3s ease;
}

.site-navbar.scrolled { box-shadow: var(--shadow-soft); }

.navbar-inner {
    width: 100%;
    max-width: 1180px;
    margin: 0 auto;
    padding: 0 20px;
    display: flex;
    align-items: center;
    justify-content: space-between;
    gap: 16px;
}

.brand {
    display: flex;
    align-items: center;
    gap: 10px;
    font-weight: 800;
    font-size: 1.06rem;
    color: var(--text-primary);
}

.brand:hover { color: var(--text-primary); }

.brand-mark {
    width: 36px;
    height: 36px;
    border-radius: 10px;
    background: var(--gradient);
    display: grid;
    place-items: center;
    color: #fff;
    font-size: 1rem;
    box-shadow: 0 6px 18px rgba(79, 124, 255, .35);
}

.nav-links {
    display: flex;
    align-items: center;
    gap: 4px;
    list-style: none;
    margin: 0;
    padding: 0;
}

.nav-links a {
    display: block;
    padding: 8px 13px;
    border-radius: 9px;
    font-size: .92rem;
    font-weight: 500;
    color: var(--text-secondary);
}

.nav-links a:hover {
    color: var(--text-primary);
    background: var(--bg-card);
}

.nav-links a.active {
    color: #fff;
    background: var(--gradient);
    box-shadow: 0 6px 16px rgba(79, 124, 255, .32);
}

.navbar-actions {
    display: flex;
    align-items: center;
    gap: 8px;
}

/* Hamburger button - only visible on small screens */
.navbar-toggle {
    display: none;
    background: var(--bg-card);
    border: 1px solid var(--border-color);
    color: var(--text-primary);
    width: 42px;
    height: 42px;
    border-radius: 10px;
    cursor: pointer;
    align-items: center;
    justify-content: center;
}

@media (max-width: 991px) {
    .navbar-toggle { display: inline-flex; }

    .nav-links {
        position: absolute;
        top: var(--navbar-height);
        left: 0;
        right: 0;
        flex-direction: column;
        align-items: stretch;
        gap: 2px;
        padding: 12px 20px 18px;
        background: var(--bg-secondary);
        border-bottom: 1px solid var(--border-color);
        box-shadow: var(--shadow-soft);
        transform: translateY(-12px);
        opacity: 0;
        visibility: hidden;
        transition: opacity .25s ease, transform .25s ease, visibility .25s;
    }

    .nav-links.open {
        transform: translateY(0);
        opacity: 1;
        visibility: visible;
    }

    .nav-links a { padding: 12px 14px; }
}

/* ==========================================================================
   6. BUTTONS
   ========================================================================== */
.btn {
    display: inline-flex;
    align-items: center;
    justify-content: center;
    gap: 8px;
    padding: 11px 22px;
    border-radius: 11px;
    border: 1px solid transparent;
    font-size: .93rem;
    font-weight: 600;
    line-height: 1.2;
    cursor: pointer;
    transition: transform .18s ease, box-shadow .18s ease, background-color .18s ease, color .18s ease;
    white-space: nowrap;
}

.btn:active { transform: translateY(1px); }

.btn-primary {
    background: var(--gradient);
    color: #fff;
    box-shadow: 0 10px 26px rgba(79, 124, 255, .32);
}

.btn-primary:hover {
    color: #fff;
    transform: translateY(-2px);
    box-shadow: 0 16px 34px rgba(79, 124, 255, .42);
}

.btn-outline {
    background: transparent;
    color: var(--text-primary);
    border-color: var(--border-color);
}

.btn-outline:hover {
    color: var(--text-primary);
    background: var(--bg-card-hover);
    border-color: var(--accent-solid);
    transform: translateY(-2px);
}

.btn-ghost {
    background: var(--bg-card);
    color: var(--text-primary);
    border-color: var(--border-color);
}

.btn-ghost:hover { background: var(--bg-card-hover); color: var(--text-primary); }

.btn-sm { padding: 7px 14px; font-size: .84rem; border-radius: 9px; }
.btn-lg { padding: 14px 28px; font-size: 1rem; }
.btn-block { width: 100%; }

.btn-danger { background: #dc3545; color: #fff; }
.btn-danger:hover { background: #c82333; color: #fff; }
.btn-success { background: #198754; color: #fff; }
.btn-success:hover { background: #157347; color: #fff; }
.btn-warning { background: #f0a92b; color: #212529; }
.btn-warning:hover { background: #e09b17; color: #212529; }

/* Small round icon button (theme toggle) */
.icon-btn {
    width: 42px;
    height: 42px;
    display: inline-flex;
    align-items: center;
    justify-content: center;
    border-radius: 11px;
    border: 1px solid var(--border-color);
    background: var(--bg-card);
    color: var(--text-primary);
    cursor: pointer;
    transition: transform .2s ease, background-color .2s ease;
}

.icon-btn:hover { transform: translateY(-2px); background: var(--bg-card-hover); }

/* ==========================================================================
   7. CARDS + GLASSMORPHISM
   ========================================================================== */
.card-glass {
    position: relative;
    background: var(--bg-card);
    border: 1px solid var(--border-color);
    border-radius: var(--radius);
    padding: 26px;
    backdrop-filter: blur(12px);
    -webkit-backdrop-filter: blur(12px);
    box-shadow: var(--shadow-soft);
    transition: transform .25s ease, box-shadow .25s ease, background-color .25s ease,
                border-color .25s ease;
    height: 100%;
    display: flex;
    flex-direction: column;
}

.card-glass:hover {
    transform: translateY(-6px);
    background: var(--bg-card-hover);
    border-color: rgba(109, 141, 255, .40);
    box-shadow: var(--glow), var(--shadow-lift);
}

.card-glass .card-body-flex {
    flex: 1 1 auto;
    display: flex;
    flex-direction: column;
}

.card-title { font-size: 1.12rem; margin-bottom: 8px; }
.card-text { color: var(--text-secondary); font-size: .94rem; margin-bottom: 14px; }

/* Coloured top edge that appears on hover */
.card-glass::after {
    content: "";
    position: absolute;
    inset: 0 0 auto 0;
    height: 3px;
    border-radius: var(--radius) var(--radius) 0 0;
    background: var(--gradient);
    opacity: 0;
    transition: opacity .25s ease;
}

.card-glass:hover::after { opacity: 1; }

/* ==========================================================================
   8. BADGES / CHIPS
   ========================================================================== */
.badge {
    display: inline-flex;
    align-items: center;
    gap: 5px;
    padding: 5px 11px;
    border-radius: 999px;
    font-size: .76rem;
    font-weight: 600;
    line-height: 1.3;
    border: 1px solid var(--border-color);
    background: var(--bg-card);
    color: var(--text-secondary);
}

.badge-gradient {
    background: var(--gradient);
    color: #fff;
    border-color: transparent;
}

.badge-soft {
    background: color-mix(in srgb, var(--accent-start) 16%, transparent);
    color: var(--accent-solid);
    border-color: color-mix(in srgb, var(--accent-start) 32%, transparent);
}

.badge-danger  { background: rgba(220,53,69,.16);  color: #ff8b96; border-color: rgba(220,53,69,.35); }
.badge-warning { background: rgba(240,169,43,.16); color: #f4c46d; border-color: rgba(240,169,43,.35); }
.badge-success { background: rgba(25,135,84,.16);  color: #6fd6a5; border-color: rgba(25,135,84,.35); }
.badge-info    { background: rgba(13,202,240,.16); color: #6fd3e8; border-color: rgba(13,202,240,.35); }

html[data-theme="light"] .badge-danger  { color: #b02a37; }
html[data-theme="light"] .badge-warning { color: #9a6700; }
html[data-theme="light"] .badge-success { color: #0f6b41; }
html[data-theme="light"] .badge-info    { color: #087990; }

.chip-row { display: flex; flex-wrap: wrap; gap: 7px; }

/* ==========================================================================
   9. HERO
   ========================================================================== */
.hero {
    padding: 78px 0 62px;
    position: relative;
}

.hero-grid {
    display: grid;
    grid-template-columns: 1.15fr .85fr;
    gap: 46px;
    align-items: center;
}

@media (max-width: 900px) {
    .hero-grid { grid-template-columns: 1fr; text-align: center; gap: 34px; }
    .hero-actions, .hero-socials { justify-content: center; }
    .hero-avatar-wrap { order: -1; }
}

.hero-eyebrow {
    display: inline-flex;
    align-items: center;
    gap: 8px;
    padding: 7px 14px;
    border-radius: 999px;
    border: 1px solid var(--border-color);
    background: var(--bg-card);
    color: var(--text-secondary);
    font-size: .82rem;
    font-weight: 600;
    margin-bottom: 18px;
}

.hero-title { margin-bottom: 10px; }

.hero-name {
    background: var(--gradient);
    -webkit-background-clip: text;
    background-clip: text;
    color: transparent;
}

.hero-typing-line {
    font-size: clamp(1rem, 2.1vw, 1.28rem);
    font-weight: 600;
    color: var(--text-primary);
    margin-bottom: 16px;
    min-height: 1.8em;
}

.hero-typing-line .cursor {
    display: inline-block;
    width: 2px;
    height: 1.05em;
    margin-left: 3px;
    vertical-align: text-bottom;
    background: var(--accent-solid);
    animation: blink 1s step-end infinite;
}

@keyframes blink { 50% { opacity: 0; } }

.hero-intro {
    color: var(--text-secondary);
    max-width: 560px;
    margin-bottom: 26px;
}

@media (max-width: 900px) { .hero-intro { margin-left: auto; margin-right: auto; } }

.hero-actions { display: flex; flex-wrap: wrap; gap: 12px; margin-bottom: 24px; }

.hero-socials { display: flex; flex-wrap: wrap; gap: 10px; }

.hero-avatar-wrap {
    display: grid;
    place-items: center;
    position: relative;
}

.hero-avatar {
    width: min(340px, 76vw);
    aspect-ratio: 1 / 1;
    border-radius: 50%;
    object-fit: cover;
    border: 4px solid transparent;
    background: var(--gradient) border-box;
    box-shadow: var(--shadow-lift), 0 0 60px rgba(109, 141, 255, .22);
    animation: avatarFloat 6s ease-in-out infinite;
}

@keyframes avatarFloat {
    0%, 100% { transform: translateY(0); }
    50%      { transform: translateY(-12px); }
}

/* Floating stat pills around the avatar */
.hero-float {
    position: absolute;
    padding: 9px 15px;
    border-radius: 12px;
    background: var(--bg-card);
    border: 1px solid var(--border-color);
    backdrop-filter: blur(10px);
    -webkit-backdrop-filter: blur(10px);
    box-shadow: var(--shadow-soft);
    font-size: .82rem;
    font-weight: 700;
    color: var(--text-primary);
    animation: avatarFloat 7s ease-in-out infinite;
}

.hero-float.f1 { top: 8%;  left: -4%;  animation-delay: -2s; }
.hero-float.f2 { bottom: 12%; right: -6%; animation-delay: -4s; }

@media (max-width: 900px) { .hero-float { display: none; } }

/* ==========================================================================
   10. STATISTICS
   ========================================================================== */
.stat-card {
    text-align: center;
    padding: 24px 18px;
}

.stat-value {
    font-size: 2.1rem;
    font-weight: 800;
    line-height: 1.1;
    background: var(--gradient);
    -webkit-background-clip: text;
    background-clip: text;
    color: transparent;
}

.stat-label {
    font-size: .84rem;
    font-weight: 600;
    color: var(--text-muted);
    text-transform: uppercase;
    letter-spacing: .08em;
    margin-top: 4px;
}

/* ==========================================================================
   11. AVATAR / PROFILE
   ========================================================================== */
.about-avatar {
    width: 100%;
    max-width: 330px;
    aspect-ratio: 1 / 1;
    border-radius: 24px;
    object-fit: cover;
    border: 1px solid var(--border-color);
    box-shadow: var(--shadow-lift);
}

.about-grid {
    display: grid;
    grid-template-columns: .8fr 1.2fr;
    gap: 42px;
    align-items: start;
}

@media (max-width: 900px) { .about-grid { grid-template-columns: 1fr; text-align: center; } }

.info-list {
    list-style: none;
    padding: 0;
    margin: 0;
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 12px 22px;
}

@media (max-width: 640px) { .info-list { grid-template-columns: 1fr; } }

.info-list li {
    display: flex;
    flex-direction: column;
    gap: 2px;
    text-align: left;
}

.info-list .info-key {
    font-size: .74rem;
    font-weight: 700;
    letter-spacing: .09em;
    text-transform: uppercase;
    color: var(--text-muted);
}

.info-list .info-val { color: var(--text-primary); font-weight: 500; font-size: .95rem; }

/* ==========================================================================
   12. SKILLS
   ========================================================================== */
.skill-item { margin-bottom: 20px; }

.skill-head {
    display: flex;
    justify-content: space-between;
    align-items: baseline;
    margin-bottom: 7px;
}

.skill-name { font-weight: 600; font-size: .94rem; color: var(--text-primary); }

.skill-pct { font-size: .82rem; font-weight: 700; color: var(--accent-solid); }

.progress-track {
    height: 8px;
    border-radius: 999px;
    background: color-mix(in srgb, var(--text-muted) 22%, transparent);
    overflow: hidden;
}

.progress-fill {
    height: 100%;
    width: 0;
    border-radius: 999px;
    background: var(--gradient);
    transition: width 1.1s cubic-bezier(.22, 1, .36, 1);
}

/* Colour variants driven by Skill.getBarClass() */
.progress-fill.bg-success { background: linear-gradient(90deg, #17c964, #0fb55c); }
.progress-fill.bg-info    { background: linear-gradient(90deg, #22b8f0, #4f7cff); }
.progress-fill.bg-warning { background: linear-gradient(90deg, #f5b73d, #f08c1e); }
.progress-fill.bg-danger  { background: linear-gradient(90deg, #f26d6d, #dc3545); }

/* ==========================================================================
   13. PROJECTS
   ========================================================================== */
.filter-bar {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    gap: 9px;
    margin-bottom: 38px;
}

.filter-btn {
    padding: 8px 18px;
    border-radius: 999px;
    border: 1px solid var(--border-color);
    background: var(--bg-card);
    color: var(--text-secondary);
    font-size: .88rem;
    font-weight: 600;
    cursor: pointer;
    transition: all .2s ease;
}

.filter-btn:hover { color: var(--text-primary); border-color: var(--accent-solid); }

.filter-btn.active {
    background: var(--gradient);
    color: #fff;
    border-color: transparent;
    box-shadow: 0 8px 20px rgba(79, 124, 255, .30);
}

.project-thumb {
    position: relative;
    aspect-ratio: 16 / 9;
    border-radius: var(--radius-sm);
    overflow: hidden;
    margin-bottom: 16px;
    background: color-mix(in srgb, var(--accent-start) 12%, var(--bg-secondary));
    display: grid;
    place-items: center;
}

.project-thumb img {
    width: 100%;
    height: 100%;
    object-fit: cover;
    transition: transform .45s ease;
}

.card-glass:hover .project-thumb img { transform: scale(1.06); }

.project-thumb .thumb-badge {
    position: absolute;
    top: 10px;
    left: 10px;
    padding: 4px 10px;
    border-radius: 999px;
    font-size: .72rem;
    font-weight: 700;
    background: rgba(10, 14, 23, .72);
    color: #fff;
    backdrop-filter: blur(6px);
}

.project-actions {
    display: flex;
    flex-wrap: wrap;
    gap: 8px;
    margin-top: auto;
    padding-top: 6px;
}

/* ==========================================================================
   14. TIMELINE
   ========================================================================== */
.timeline {
    position: relative;
    padding-left: 34px;
    max-width: 860px;
    margin: 0 auto;
}

.timeline::before {
    content: "";
    position: absolute;
    left: 8px;
    top: 6px;
    bottom: 6px;
    width: 2px;
    background: linear-gradient(to bottom, var(--accent-start), var(--accent-end));
    opacity: .45;
}

.timeline-item { position: relative; padding-bottom: 30px; }

.timeline-item:last-child { padding-bottom: 0; }

.timeline-dot {
    position: absolute;
    left: -34px;
    top: 6px;
    width: 18px;
    height: 18px;
    border-radius: 50%;
    background: var(--gradient);
    border: 3px solid var(--bg-primary);
    box-shadow: 0 0 0 3px color-mix(in srgb, var(--accent-start) 32%, transparent);
}

.timeline-date {
    font-size: .79rem;
    font-weight: 700;
    letter-spacing: .06em;
    text-transform: uppercase;
    color: var(--accent-solid);
    margin-bottom: 6px;
}

.timeline-card {
    background: var(--bg-card);
    border: 1px solid var(--border-color);
    border-radius: var(--radius);
    padding: 20px 22px;
    transition: transform .25s ease, border-color .25s ease;
}

.timeline-card:hover { transform: translateX(4px); border-color: var(--accent-solid); }

.timeline-card h3 { margin-bottom: 4px; font-size: 1.1rem; }
.timeline-sub { color: var(--text-muted); font-size: .9rem; margin-bottom: 10px; }

.bullet-list {
    list-style: none;
    padding: 0;
    margin: 0 0 12px;
}

.bullet-list li {
    position: relative;
    padding-left: 20px;
    margin-bottom: 7px;
    color: var(--text-secondary);
    font-size: .93rem;
}

.bullet-list li::before {
    content: "";
    position: absolute;
    left: 2px;
    top: .62em;
    width: 7px;
    height: 7px;
    border-radius: 50%;
    background: var(--gradient);
}

/* ==========================================================================
   15. CERTIFICATES
   ========================================================================== */
.cert-thumb {
    aspect-ratio: 4 / 3;
    border-radius: var(--radius-sm);
    overflow: hidden;
    margin-bottom: 15px;
    background: var(--bg-secondary);
    display: grid;
    place-items: center;
    border: 1px solid var(--border-color);
}

.cert-thumb img { width: 100%; height: 100%; object-fit: cover; }

/* ==========================================================================
   16. SERVICES
   ========================================================================== */
.service-icon {
    width: 54px;
    height: 54px;
    border-radius: 15px;
    display: grid;
    place-items: center;
    font-size: 1.5rem;
    background: color-mix(in srgb, var(--accent-start) 16%, transparent);
    color: var(--accent-solid);
    margin-bottom: 16px;
    transition: transform .3s ease;
}

.card-glass:hover .service-icon { transform: scale(1.08) rotate(-4deg); }

/* ==========================================================================
   17. FORMS
   ========================================================================== */
.form-group { margin-bottom: 18px; }

.form-label {
    display: block;
    font-size: .84rem;
    font-weight: 600;
    color: var(--text-primary);
    margin-bottom: 6px;
}

.form-label .req { color: #ff6b78; margin-left: 2px; }

.form-control,
.form-select,
textarea.form-control {
    width: 100%;
    padding: 11px 14px;
    border-radius: var(--radius-sm);
    border: 1px solid var(--border-color);
    background: color-mix(in srgb, var(--bg-secondary) 70%, transparent);
    color: var(--text-primary);
    font-size: .94rem;
    font-family: inherit;
    transition: border-color .2s ease, box-shadow .2s ease;
}

.form-control::placeholder { color: var(--text-muted); }

.form-control:focus,
.form-select:focus {
    outline: none;
    border-color: var(--accent-solid);
    box-shadow: 0 0 0 3px color-mix(in srgb, var(--accent-start) 22%, transparent);
}

.form-control.is-invalid { border-color: #ff6b78; }

textarea.form-control { min-height: 130px; resize: vertical; }

.form-text {
    display: block;
    font-size: .79rem;
    color: var(--text-muted);
    margin-top: 5px;
}

.invalid-feedback {
    display: block;
    font-size: .8rem;
    color: #ff7b86;
    margin-top: 5px;
}

html[data-theme="light"] .invalid-feedback { color: #c02632; }

.form-row { display: flex; gap: 16px; flex-wrap: wrap; }
.form-row > * { flex: 1 1 220px; }

.form-check {
    display: flex;
    align-items: center;
    gap: 9px;
    font-size: .9rem;
    color: var(--text-secondary);
    cursor: pointer;
}

.form-check input[type="checkbox"] {
    width: 18px;
    height: 18px;
    accent-color: var(--accent-solid);
}

/* ==========================================================================
   18. ALERTS / TOASTS
   ========================================================================== */
.alert {
    padding: 13px 18px;
    border-radius: var(--radius-sm);
    border: 1px solid transparent;
    font-size: .92rem;
    margin-bottom: 18px;
    display: flex;
    align-items: flex-start;
    gap: 10px;
}

.alert-success {
    background: rgba(25, 135, 84, .14);
    border-color: rgba(25, 135, 84, .38);
    color: #6fd6a5;
}

.alert-danger {
    background: rgba(220, 53, 69, .14);
    border-color: rgba(220, 53, 69, .38);
    color: #ff8b96;
}

.alert-warning {
    background: rgba(240, 169, 43, .14);
    border-color: rgba(240, 169, 43, .38);
    color: #f4c46d;
}

.alert-info {
    background: color-mix(in srgb, var(--accent-start) 14%, transparent);
    border-color: color-mix(in srgb, var(--accent-start) 34%, transparent);
    color: var(--accent-solid);
}

html[data-theme="light"] .alert-success { color: #0f6b41; }
html[data-theme="light"] .alert-danger  { color: #b02a37; }
html[data-theme="light"] .alert-warning { color: #9a6700; }

/* Toast container (top-right, driven by app.js) */
#toastContainer {
    position: fixed;
    top: 88px;
    right: 20px;
    z-index: 1090;
    display: flex;
    flex-direction: column;
    gap: 10px;
    max-width: min(360px, calc(100vw - 40px));
}

.toast-item {
    padding: 13px 17px;
    border-radius: 12px;
    background: var(--bg-secondary);
    border: 1px solid var(--border-color);
    box-shadow: var(--shadow-lift);
    color: var(--text-primary);
    font-size: .9rem;
    display: flex;
    align-items: center;
    gap: 10px;
    animation: toastIn .3s cubic-bezier(.22, 1, .36, 1);
}

.toast-item.success { border-left: 4px solid #198754; }
.toast-item.error   { border-left: 4px solid #dc3545; }
.toast-item.info    { border-left: 4px solid var(--accent-solid); }

.toast-item.hide { animation: toastOut .25s ease forwards; }

@keyframes toastIn  { from { opacity: 0; transform: translateX(30px); } to { opacity: 1; transform: none; } }
@keyframes toastOut { to   { opacity: 0; transform: translateX(30px); } }

/* ==========================================================================
   19. TABLES
   ========================================================================== */
.table-wrap {
    overflow-x: auto;
    border: 1px solid var(--border-color);
    border-radius: var(--radius);
    background: var(--bg-card);
}

.data-table {
    width: 100%;
    border-collapse: collapse;
    font-size: .91rem;
    min-width: 640px;
}

.data-table thead th {
    text-align: left;
    padding: 13px 16px;
    font-size: .74rem;
    font-weight: 700;
    letter-spacing: .08em;
    text-transform: uppercase;
    color: var(--text-muted);
    border-bottom: 1px solid var(--border-color);
    white-space: nowrap;
}

.data-table tbody td {
    padding: 13px 16px;
    border-bottom: 1px solid var(--border-color);
    color: var(--text-secondary);
    vertical-align: middle;
}

.data-table tbody tr:last-child td { border-bottom: none; }

.data-table tbody tr { transition: background-color .18s ease; }
.data-table tbody tr:hover { background: var(--bg-card-hover); }

.data-table td strong { color: var(--text-primary); font-weight: 600; }

.action-row { display: flex; gap: 6px; flex-wrap: wrap; }

/* ==========================================================================
   20. FOOTER
   ========================================================================== */
.site-footer {
    border-top: 1px solid var(--border-color);
    background: var(--bg-secondary);
    padding: 46px 0 26px;
    margin-top: 30px;
}

.footer-grid {
    display: grid;
    grid-template-columns: 1.4fr 1fr 1fr;
    gap: 34px;
    margin-bottom: 30px;
}

@media (max-width: 780px) { .footer-grid { grid-template-columns: 1fr; gap: 26px; } }

.footer-title {
    font-size: .82rem;
    font-weight: 700;
    letter-spacing: .1em;
    text-transform: uppercase;
    color: var(--text-primary);
    margin-bottom: 12px;
}

.footer-links { list-style: none; padding: 0; margin: 0; }

.footer-links li { margin-bottom: 8px; }

.footer-links a { color: var(--text-muted); font-size: .9rem; }
.footer-links a:hover { color: var(--accent-solid); }

.footer-bottom {
    border-top: 1px solid var(--border-color);
    padding-top: 20px;
    display: flex;
    flex-wrap: wrap;
    justify-content: space-between;
    gap: 12px;
    font-size: .85rem;
    color: var(--text-muted);
}

.social-row { display: flex; gap: 9px; flex-wrap: wrap; }

.social-link {
    width: 40px;
    height: 40px;
    display: grid;
    place-items: center;
    border-radius: 11px;
    border: 1px solid var(--border-color);
    background: var(--bg-card);
    color: var(--text-secondary);
    font-size: 1rem;
    transition: transform .2s ease, color .2s ease, border-color .2s ease;
}

.social-link:hover {
    transform: translateY(-3px);
    color: #fff;
    background: var(--gradient);
    border-color: transparent;
}

/* ==========================================================================
   21. BACK TO TOP
   ========================================================================== */
#backToTop {
    position: fixed;
    right: 22px;
    bottom: 22px;
    z-index: 1050;
    width: 46px;
    height: 46px;
    border-radius: 50%;
    border: none;
    background: var(--gradient);
    color: #fff;
    font-size: 1.05rem;
    cursor: pointer;
    box-shadow: 0 10px 26px rgba(79, 124, 255, .38);
    opacity: 0;
    visibility: hidden;
    transform: translateY(12px);
    transition: opacity .25s ease, transform .25s ease, visibility .25s;
}

#backToTop.show { opacity: 1; visibility: visible; transform: none; }
#backToTop:hover { transform: translateY(-3px); }

/* ==========================================================================
   22. SCROLL REVEAL ANIMATION
   ========================================================================== */
.reveal {
    opacity: 0;
    transform: translateY(22px);
    transition: opacity .6s ease, transform .6s ease;
}

.reveal.visible { opacity: 1; transform: none; }

/* Stagger children a little */
.reveal-delay-1 { transition-delay: .08s; }
.reveal-delay-2 { transition-delay: .16s; }
.reveal-delay-3 { transition-delay: .24s; }

/* ==========================================================================
   23. EMPTY STATE
   ========================================================================== */
.empty-state {
    text-align: center;
    padding: 54px 24px;
    border: 1px dashed var(--border-color);
    border-radius: var(--radius);
    background: var(--bg-card);
}

.empty-state .empty-icon { font-size: 2.2rem; margin-bottom: 10px; opacity: .6; }
.empty-state p { margin: 0; color: var(--text-muted); }

/* ==========================================================================
   24. PAGE HEADER (inner pages)
   ========================================================================== */
.page-header {
    padding: 58px 0 34px;
    text-align: center;
    border-bottom: 1px solid var(--border-color);
    background:
        radial-gradient(600px 240px at 50% -60px,
            color-mix(in srgb, var(--accent-start) 22%, transparent), transparent);
}

.page-header h1 { font-size: clamp(1.8rem, 4vw, 2.6rem); margin-bottom: 8px; }
.page-header p { color: var(--text-muted); max-width: 640px; margin: 0 auto; }

.breadcrumb-line {
    font-size: .82rem;
    color: var(--text-muted);
    margin-bottom: 12px;
}

.breadcrumb-line a { color: var(--text-muted); }
.breadcrumb-line a:hover { color: var(--accent-solid); }

/* ==========================================================================
   25. UTILITIES
   ========================================================================== */
.text-center { text-align: center; }
.text-muted  { color: var(--text-muted); }
.mt-1 { margin-top: 8px; }   .mt-2 { margin-top: 16px; }  .mt-3 { margin-top: 26px; }
.mb-1 { margin-bottom: 8px; } .mb-2 { margin-bottom: 16px; } .mb-3 { margin-bottom: 26px; }
.gap-row { display: flex; gap: 12px; flex-wrap: wrap; align-items: center; }
.spread { display: flex; justify-content: space-between; align-items: center; gap: 14px; flex-wrap: wrap; }
.divider { height: 1px; background: var(--border-color); margin: 26px 0; }

/* Detail page key/value grid */
.detail-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 18px;
}

@media (max-width: 780px) { .detail-grid { grid-template-columns: 1fr; } }

.detail-block {
    background: var(--bg-card);
    border: 1px solid var(--border-color);
    border-radius: var(--radius);
    padding: 22px;
}

.detail-block h3 { font-size: 1rem; margin-bottom: 12px; }

```

---

## `portfolio-app/src/main/resources/static/css/admin.css`
<a id="portfolio-app-src-main-resources-static-css-admincss"></a>

```css
/* ==========================================================================
   ADMIN PANEL STYLES
   ==========================================================================
   Loaded AFTER style.css so it can reuse every variable and component
   (.card-glass, .btn, .form-control, .data-table, ...) and only add the
   dashboard-specific layout: a fixed sidebar plus a content area.
   ========================================================================== */

/* --------------------------------------------------------------------------
   1. LOGIN PAGE
   -------------------------------------------------------------------------- */
.login-page {
    min-height: 100vh;
    display: grid;
    place-items: center;
    padding: 30px 18px;
}

.login-card {
    width: 100%;
    max-width: 430px;
    background: var(--bg-card);
    border: 1px solid var(--border-color);
    border-radius: 22px;
    padding: 38px 34px;
    backdrop-filter: blur(14px);
    -webkit-backdrop-filter: blur(14px);
    box-shadow: var(--shadow-lift);
    animation: loginIn .5s cubic-bezier(.22, 1, .36, 1);
}

@keyframes loginIn {
    from { opacity: 0; transform: translateY(18px) scale(.98); }
    to   { opacity: 1; transform: none; }
}

.login-logo {
    width: 62px;
    height: 62px;
    margin: 0 auto 18px;
    border-radius: 18px;
    background: var(--gradient);
    display: grid;
    place-items: center;
    color: #fff;
    font-size: 1.7rem;
    box-shadow: 0 12px 30px rgba(79, 124, 255, .38);
}

.login-card h1 {
    font-size: 1.45rem;
    text-align: center;
    margin-bottom: 6px;
}

.login-subtitle {
    text-align: center;
    color: var(--text-muted);
    font-size: .9rem;
    margin-bottom: 26px;
}

.login-hint {
    margin-top: 20px;
    padding: 12px 14px;
    border-radius: 11px;
    background: color-mix(in srgb, var(--accent-start) 10%, transparent);
    border: 1px solid color-mix(in srgb, var(--accent-start) 24%, transparent);
    font-size: .8rem;
    color: var(--text-muted);
    line-height: 1.55;
}

.login-hint code {
    color: var(--accent-solid);
    background: transparent;
    font-weight: 700;
}

.login-back {
    display: block;
    text-align: center;
    margin-top: 20px;
    font-size: .86rem;
    color: var(--text-muted);
}

/* --------------------------------------------------------------------------
   2. ADMIN SHELL (sidebar + content)
   -------------------------------------------------------------------------- */
.admin-shell {
    display: grid;
    grid-template-columns: 264px 1fr;
    min-height: 100vh;
}

.admin-sidebar {
    background: var(--bg-secondary);
    border-right: 1px solid var(--border-color);
    padding: 22px 16px;
    position: sticky;
    top: 0;
    height: 100vh;
    overflow-y: auto;
    display: flex;
    flex-direction: column;
    gap: 6px;
}

.sidebar-brand {
    display: flex;
    align-items: center;
    gap: 10px;
    padding: 6px 8px 18px;
    font-weight: 800;
    color: var(--text-primary);
    font-size: 1rem;
}

.sidebar-brand:hover { color: var(--text-primary); }

.sidebar-label {
    font-size: .7rem;
    font-weight: 700;
    letter-spacing: .12em;
    text-transform: uppercase;
    color: var(--text-muted);
    padding: 16px 10px 7px;
}

.sidebar-link {
    display: flex;
    align-items: center;
    gap: 11px;
    padding: 10px 12px;
    border-radius: 11px;
    color: var(--text-secondary);
    font-size: .92rem;
    font-weight: 500;
    transition: background-color .18s ease, color .18s ease;
}

.sidebar-link:hover {
    background: var(--bg-card);
    color: var(--text-primary);
}

.sidebar-link.active {
    background: var(--gradient);
    color: #fff;
    box-shadow: 0 8px 20px rgba(79, 124, 255, .30);
}

.sidebar-link .ico { font-size: 1rem; width: 20px; text-align: center; }

.sidebar-link .count-pill {
    margin-left: auto;
    min-width: 22px;
    padding: 1px 7px;
    border-radius: 999px;
    background: #dc3545;
    color: #fff;
    font-size: .72rem;
    font-weight: 700;
    text-align: center;
}

.sidebar-footer { margin-top: auto; padding-top: 16px; }

/* Mobile: the sidebar becomes a slide-in drawer */
.sidebar-backdrop {
    position: fixed;
    inset: 0;
    background: rgba(0, 0, 0, .55);
    z-index: 1040;
    opacity: 0;
    visibility: hidden;
    transition: opacity .25s ease, visibility .25s;
}

.sidebar-backdrop.show { opacity: 1; visibility: visible; }

@media (max-width: 991px) {
    .admin-shell { grid-template-columns: 1fr; }

    .admin-sidebar {
        position: fixed;
        left: 0;
        top: 0;
        width: 264px;
        z-index: 1050;
        transform: translateX(-100%);
        transition: transform .28s cubic-bezier(.22, 1, .36, 1);
    }

    .admin-sidebar.open { transform: translateX(0); }
}

/* --------------------------------------------------------------------------
   3. ADMIN TOP BAR + CONTENT
   -------------------------------------------------------------------------- */
.admin-main {
    min-width: 0;
    display: flex;
    flex-direction: column;
}

.admin-topbar {
    position: sticky;
    top: 0;
    z-index: 1020;
    height: 66px;
    display: flex;
    align-items: center;
    justify-content: space-between;
    gap: 14px;
    padding: 0 24px;
    background: color-mix(in srgb, var(--bg-primary) 82%, transparent);
    backdrop-filter: blur(12px);
    -webkit-backdrop-filter: blur(12px);
    border-bottom: 1px solid var(--border-color);
}

.admin-topbar h1 {
    font-size: 1.16rem;
    margin: 0;
    white-space: nowrap;
    overflow: hidden;
    text-overflow: ellipsis;
}

.admin-content { padding: 26px 24px 46px; flex: 1 1 auto; }

@media (max-width: 640px) {
    .admin-content { padding: 20px 16px 40px; }
    .admin-topbar { padding: 0 16px; }
}

.sidebar-toggle {
    display: none;
    width: 40px;
    height: 40px;
    border-radius: 10px;
    border: 1px solid var(--border-color);
    background: var(--bg-card);
    color: var(--text-primary);
    cursor: pointer;
    align-items: center;
    justify-content: center;
}

@media (max-width: 991px) { .sidebar-toggle { display: inline-flex; } }

/* --------------------------------------------------------------------------
   4. STAT CARDS
   -------------------------------------------------------------------------- */
.stat-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(178px, 1fr));
    gap: 16px;
    margin-bottom: 28px;
}

.stat-tile {
    background: var(--bg-card);
    border: 1px solid var(--border-color);
    border-radius: var(--radius);
    padding: 20px;
    display: flex;
    align-items: center;
    gap: 15px;
    transition: transform .22s ease, border-color .22s ease, box-shadow .22s ease;
}

.stat-tile:hover {
    transform: translateY(-4px);
    border-color: color-mix(in srgb, var(--accent-start) 42%, transparent);
    box-shadow: var(--glow);
}

.stat-tile .tile-icon {
    width: 48px;
    height: 48px;
    flex: 0 0 48px;
    border-radius: 14px;
    display: grid;
    place-items: center;
    font-size: 1.35rem;
    color: #fff;
}

.tile-icon.c1 { background: linear-gradient(135deg, #4f7cff, #6d8dff); }
.tile-icon.c2 { background: linear-gradient(135deg, #9b5cff, #c07cff); }
.tile-icon.c3 { background: linear-gradient(135deg, #17c964, #3ddc84); }
.tile-icon.c4 { background: linear-gradient(135deg, #f5a623, #f7c65b); }
.tile-icon.c5 { background: linear-gradient(135deg, #22b8f0, #5ccbf5); }
.tile-icon.c6 { background: linear-gradient(135deg, #f26d6d, #ff8b96); }
.tile-icon.c7 { background: linear-gradient(135deg, #12b5a5, #3ed6c7); }
.tile-icon.c8 { background: linear-gradient(135deg, #8b5cf6, #a78bfa); }

.stat-tile .tile-value {
    font-size: 1.62rem;
    font-weight: 800;
    line-height: 1.1;
    color: var(--text-primary);
}

.stat-tile .tile-label {
    font-size: .8rem;
    color: var(--text-muted);
    font-weight: 600;
    text-transform: uppercase;
    letter-spacing: .05em;
}

/* --------------------------------------------------------------------------
   5. ADMIN PANEL HELPERS
   -------------------------------------------------------------------------- */
.panel {
    background: var(--bg-card);
    border: 1px solid var(--border-color);
    border-radius: var(--radius);
    padding: 22px;
    margin-bottom: 22px;
}

.panel-head {
    display: flex;
    align-items: center;
    justify-content: space-between;
    gap: 12px;
    flex-wrap: wrap;
    margin-bottom: 18px;
}

.panel-head h2 { font-size: 1.08rem; margin: 0; }
.panel-head p { margin: 0; font-size: .86rem; color: var(--text-muted); }

.admin-grid-2 {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 22px;
}

@media (max-width: 900px) { .admin-grid-2 { grid-template-columns: 1fr; } }

.mini-list { list-style: none; padding: 0; margin: 0; }

.mini-list li {
    display: flex;
    align-items: center;
    justify-content: space-between;
    gap: 12px;
    padding: 11px 0;
    border-bottom: 1px solid var(--border-color);
    font-size: .9rem;
}

.mini-list li:last-child { border-bottom: none; }

.mini-list .mini-title {
    color: var(--text-primary);
    font-weight: 600;
    overflow: hidden;
    text-overflow: ellipsis;
    white-space: nowrap;
}

.mini-list .mini-meta { color: var(--text-muted); font-size: .8rem; white-space: nowrap; }

/* Search + filter toolbar */
.toolbar {
    display: flex;
    flex-wrap: wrap;
    gap: 10px;
    align-items: center;
    margin-bottom: 20px;
}

.toolbar form { display: flex; gap: 8px; flex-wrap: wrap; align-items: center; }
.toolbar .form-control, .toolbar .form-select { width: auto; min-width: 190px; }

/* Tabs used on the settings page */
.tab-bar {
    display: flex;
    gap: 6px;
    border-bottom: 1px solid var(--border-color);
    margin-bottom: 24px;
    flex-wrap: wrap;
}

.tab-btn {
    padding: 10px 18px;
    border: none;
    background: transparent;
    color: var(--text-muted);
    font-size: .92rem;
    font-weight: 600;
    cursor: pointer;
    border-bottom: 2px solid transparent;
    margin-bottom: -1px;
    transition: color .2s ease, border-color .2s ease;
}

.tab-btn:hover { color: var(--text-primary); }

.tab-btn.active {
    color: var(--accent-solid);
    border-bottom-color: var(--accent-solid);
}

.tab-pane { display: none; }
.tab-pane.active { display: block; animation: tabIn .3s ease; }

@keyframes tabIn { from { opacity: 0; transform: translateY(6px); } to { opacity: 1; transform: none; } }

/* Confirmation dialog (built in app.js, no browser alert()) */
.confirm-backdrop {
    position: fixed;
    inset: 0;
    background: rgba(4, 7, 14, .66);
    backdrop-filter: blur(3px);
    z-index: 1100;
    display: grid;
    place-items: center;
    padding: 20px;
    animation: tabIn .2s ease;
}

.confirm-box {
    width: 100%;
    max-width: 420px;
    background: var(--bg-secondary);
    border: 1px solid var(--border-color);
    border-radius: 18px;
    padding: 26px;
    box-shadow: var(--shadow-lift);
    text-align: center;
}

.confirm-box .confirm-icon {
    width: 56px;
    height: 56px;
    margin: 0 auto 14px;
    border-radius: 50%;
    display: grid;
    place-items: center;
    font-size: 1.5rem;
    background: rgba(220, 53, 69, .15);
    color: #ff8b96;
}

.confirm-box h3 { font-size: 1.12rem; margin-bottom: 8px; }
.confirm-box p { font-size: .9rem; color: var(--text-muted); margin-bottom: 20px; }

.confirm-actions { display: flex; gap: 10px; justify-content: center; }

```

---

## `portfolio-app/src/main/resources/static/js/app.js`
<a id="portfolio-app-src-main-resources-static-js-appjs"></a>

```javascript
/* ==========================================================================
   PERSONAL PORTFOLIO - MAIN JAVASCRIPT
   ==========================================================================
   Everything here is plain JavaScript (no jQuery, no build step).
   Each feature is wrapped in its own function and guarded with an existence
   check, so a page that does not contain that element simply skips it.

   FEATURES
     1. Dark / light theme toggle (remembered in localStorage)
     2. Sticky navbar shadow + mobile hamburger menu
     3. Typing animation in the hero
     4. Scroll reveal animations (IntersectionObserver)
     5. Skill progress bars that fill when scrolled into view
     6. Client-side project filtering
     7. Toast notifications
     8. Confirmation dialogs for delete buttons
     9. Back-to-top button
    10. Contact form validation + AJAX submit
   ========================================================================== */

(function () {
    'use strict';

    /* ======================================================================
       1. DARK / LIGHT THEME
       ====================================================================== */
    function initTheme() {
        var root = document.documentElement;
        var toggle = document.getElementById('themeToggle');
        var icon = document.getElementById('themeIcon');

        function apply(theme) {
            root.setAttribute('data-theme', theme);
            localStorage.setItem('portfolio-theme', theme);
            if (icon) {
                icon.className = (theme === 'light')
                    ? 'bi bi-sun-fill'
                    : 'bi bi-moon-stars-fill';
            }
            if (toggle) {
                toggle.title = (theme === 'light')
                    ? 'Switch to dark mode'
                    : 'Switch to light mode';
            }
        }

        // Apply the stored choice (the head script already did this early to
        // avoid a flash; this call keeps the icon in sync).
        apply(localStorage.getItem('portfolio-theme') === 'light' ? 'light' : 'dark');

        if (toggle) {
            toggle.addEventListener('click', function () {
                apply(root.getAttribute('data-theme') === 'light' ? 'dark' : 'light');
            });
        }
    }

    /* ======================================================================
       2. NAVBAR
       ====================================================================== */
    function initNavbar() {
        var navbar = document.getElementById('siteNavbar');
        var toggle = document.getElementById('navbarToggle');
        var links = document.getElementById('navLinks');

        // Shadow once the page is scrolled
        function onScroll() {
            if (!navbar) return;
            navbar.classList.toggle('scrolled', window.scrollY > 10);
        }
        window.addEventListener('scroll', onScroll, { passive: true });
        onScroll();

        // Mobile hamburger
        if (toggle && links) {
            toggle.addEventListener('click', function () {
                var open = links.classList.toggle('open');
                toggle.setAttribute('aria-expanded', open ? 'true' : 'false');
            });

            // Close the menu after tapping a link (mobile UX)
            links.addEventListener('click', function (event) {
                if (event.target.tagName === 'A') {
                    links.classList.remove('open');
                    toggle.setAttribute('aria-expanded', 'false');
                }
            });

            // Close when clicking anywhere else
            document.addEventListener('click', function (event) {
                if (!navbar.contains(event.target)) {
                    links.classList.remove('open');
                    toggle.setAttribute('aria-expanded', 'false');
                }
            });
        }
    }

    /* ======================================================================
       3. TYPING ANIMATION
       ====================================================================== */
    function initTyping() {
        var target = document.getElementById('typingTarget');
        if (!target) return;

        var raw = target.getAttribute('data-words') || '';
        var words = raw.split('|').map(function (w) { return w.trim(); })
                       .filter(function (w) { return w.length > 0; });
        if (words.length === 0) return;

        // Respect the OS "reduce motion" preference
        if (window.matchMedia('(prefers-reduced-motion: reduce)').matches) {
            target.textContent = words[0];
            return;
        }

        var wordIndex = 0;
        var charIndex = 0;
        var deleting = false;

        function tick() {
            var current = words[wordIndex];

            if (!deleting) {
                charIndex++;
                target.textContent = current.substring(0, charIndex);
                if (charIndex === current.length) {
                    deleting = true;
                    setTimeout(tick, 1600);   // pause on the full word
                    return;
                }
                setTimeout(tick, 70);
            } else {
                charIndex--;
                target.textContent = current.substring(0, charIndex);
                if (charIndex === 0) {
                    deleting = false;
                    wordIndex = (wordIndex + 1) % words.length;
                    setTimeout(tick, 320);
                    return;
                }
                setTimeout(tick, 38);
            }
        }

        tick();
    }

    /* ======================================================================
       4. SCROLL REVEAL
       ====================================================================== */
    function initReveal() {
        var items = document.querySelectorAll('.reveal');
        if (items.length === 0) return;

        if (!('IntersectionObserver' in window)) {
            items.forEach(function (el) { el.classList.add('visible'); });
            return;
        }

        var observer = new IntersectionObserver(function (entries) {
            entries.forEach(function (entry) {
                if (entry.isIntersecting) {
                    entry.target.classList.add('visible');
                    observer.unobserve(entry.target);
                }
            });
        }, { threshold: 0.12, rootMargin: '0px 0px -40px 0px' });

        items.forEach(function (el) { observer.observe(el); });
    }

    /* ======================================================================
       5. SKILL PROGRESS BARS
       ====================================================================== */
    function initSkillBars() {
        var bars = document.querySelectorAll('.progress-fill[data-width]');
        if (bars.length === 0) return;

        function fill(bar) {
            var width = parseInt(bar.getAttribute('data-width'), 10) || 0;
            if (width < 0) width = 0;
            if (width > 100) width = 100;
            bar.style.width = width + '%';
        }

        if (!('IntersectionObserver' in window)) {
            bars.forEach(fill);
            return;
        }

        var observer = new IntersectionObserver(function (entries) {
            entries.forEach(function (entry) {
                if (entry.isIntersecting) {
                    fill(entry.target);
                    observer.unobserve(entry.target);
                }
            });
        }, { threshold: 0.4 });

        bars.forEach(function (bar) { observer.observe(bar); });
    }

    /* ======================================================================
       6. PROJECT FILTERING (client side, no page reload)
       ====================================================================== */
    function initProjectFilter() {
        var buttons = document.querySelectorAll('.filter-btn[data-filter]');
        var cards = document.querySelectorAll('[data-category]');
        if (buttons.length === 0 || cards.length === 0) return;

        var emptyState = document.getElementById('filterEmpty');

        buttons.forEach(function (button) {
            button.addEventListener('click', function () {
                var filter = button.getAttribute('data-filter');

                buttons.forEach(function (b) { b.classList.remove('active'); });
                button.classList.add('active');

                var visibleCount = 0;
                cards.forEach(function (card) {
                    var match = (filter === 'all') ||
                                (card.getAttribute('data-category') === filter);
                    card.style.display = match ? '' : 'none';
                    if (match) visibleCount++;
                });

                if (emptyState) {
                    emptyState.style.display = visibleCount === 0 ? '' : 'none';
                }
            });
        });
    }

    /* ======================================================================
       7. TOAST NOTIFICATIONS
       ====================================================================== */
    function showToast(message, type) {
        var container = document.getElementById('toastContainer');
        if (!container) return;

        var toast = document.createElement('div');
        toast.className = 'toast-item ' + (type || 'info');

        var iconMap = {
            success: '<i class="bi bi-check-circle-fill"></i>',
            error: '<i class="bi bi-exclamation-octagon-fill"></i>',
            info: '<i class="bi bi-info-circle-fill"></i>'
        };
        toast.innerHTML = (iconMap[type] || iconMap.info) + '<span></span>';
        toast.querySelector('span').textContent = message;

        container.appendChild(toast);

        setTimeout(function () {
            toast.classList.add('hide');
            setTimeout(function () { toast.remove(); }, 260);
        }, 3600);
    }

    // Expose globally so inline handlers / other scripts can use it
    window.showToast = showToast;

    /**
     * Converts the server-rendered flash alerts into toasts, then fades the
     * alert box out so the page does not keep a stale banner.
     */
    function initAlertToasts() {
        document.querySelectorAll('[data-autohide]').forEach(function (alertBox) {
            var type = alertBox.getAttribute('data-autohide');
            var text = alertBox.textContent.trim();
            if (text) showToast(text, type);

            setTimeout(function () {
                alertBox.style.transition = 'opacity .5s ease';
                alertBox.style.opacity = '0';
                setTimeout(function () { alertBox.remove(); }, 520);
            }, 4200);
        });
    }

    /* ======================================================================
       8. CONFIRMATION DIALOGS
       ====================================================================== */
    /**
     * Any element with data-confirm gets a custom modal instead of the
     * browser's blocking confirm().
     *
     *   <form data-confirm="Delete this project?" data-confirm-title="Delete">
     *
     * If the form posts directly (no data-confirm), nothing changes.
     */
    function initConfirmDialogs() {
        document.addEventListener('submit', function (event) {
            var form = event.target;
            if (!form.hasAttribute || !form.hasAttribute('data-confirm')) return;
            if (form.dataset.confirmed === 'true') return;

            event.preventDefault();

            var message = form.getAttribute('data-confirm');
            var title = form.getAttribute('data-confirm-title') || 'Are you sure?';
            openConfirm(title, message, function () {
                form.dataset.confirmed = 'true';
                form.requestSubmit ? form.requestSubmit() : form.submit();
            });
        });
    }

    /** Builds and shows the dialog, calling onConfirm when accepted. */
    function openConfirm(title, message, onConfirm) {
        var backdrop = document.createElement('div');
        backdrop.className = 'confirm-backdrop';
        backdrop.innerHTML =
            '<div class="confirm-box" role="dialog" aria-modal="true">' +
            '  <div class="confirm-icon"><i class="bi bi-exclamation-triangle-fill"></i></div>' +
            '  <h3></h3>' +
            '  <p></p>' +
            '  <div class="confirm-actions">' +
            '    <button type="button" class="btn btn-outline" data-cancel>Cancel</button>' +
            '    <button type="button" class="btn btn-danger" data-ok>Yes, continue</button>' +
            '  </div>' +
            '</div>';

        backdrop.querySelector('h3').textContent = title;
        backdrop.querySelector('p').textContent = message;

        function close() {
            backdrop.remove();
            document.removeEventListener('keydown', onKey);
        }

        function onKey(event) {
            if (event.key === 'Escape') close();
            if (event.key === 'Enter') { close(); onConfirm(); }
        }

        backdrop.querySelector('[data-cancel]').addEventListener('click', close);
        backdrop.querySelector('[data-ok]').addEventListener('click', function () {
            close();
            onConfirm();
        });
        backdrop.addEventListener('click', function (event) {
            if (event.target === backdrop) close();
        });
        document.addEventListener('keydown', onKey);

        document.body.appendChild(backdrop);
        backdrop.querySelector('[data-ok]').focus();
    }

    /* ======================================================================
       9. BACK TO TOP
       ====================================================================== */
    function initBackToTop() {
        var button = document.getElementById('backToTop');
        if (!button) return;

        window.addEventListener('scroll', function () {
            button.classList.toggle('show', window.scrollY > 420);
        }, { passive: true });

        button.addEventListener('click', function () {
            window.scrollTo({ top: 0, behavior: 'smooth' });
        });
    }

    /* ======================================================================
       10. CONTACT FORM  (validation + AJAX submit)
       ====================================================================== */
    function initContactForm() {
        var form = document.getElementById('contactForm');
        if (!form) return;

        var submitButton = form.querySelector('[type="submit"]');

        /** Removes any previous error marker from a field. */
        function clearError(field) {
            field.classList.remove('is-invalid');
            var next = field.nextElementSibling;
            if (next && next.classList.contains('invalid-feedback')) {
                next.remove();
            }
        }

        /** Marks a field invalid and writes the message under it. */
        function setError(field, message) {
            field.classList.add('is-invalid');
            var div = document.createElement('div');
            div.className = 'invalid-feedback';
            div.textContent = message;
            field.parentNode.insertBefore(div, field.nextSibling);
        }

        /**
         * Front-end validation.
         * The server repeats all of these checks with Bean Validation -
         * client-side checks are for speed, never for security.
         */
        function validate() {
            var valid = true;
            var emailPattern = /^[^\s@]+@[^\s@]+\.[^\s@]{2,}$/;

            [['name', 2, 'Please enter your name (at least 2 characters).'],
             ['email', 0, 'Please enter a valid email address.'],
             ['subject', 3, 'Please enter a subject (at least 3 characters).'],
             ['message', 10, 'Please write a message (at least 10 characters).']
            ].forEach(function (rule) {
                var field = form.querySelector('[name="' + rule[0] + '"]');
                if (!field) return;

                clearError(field);
                var value = field.value.trim();
                var problem = null;

                if (value.length === 0) {
                    problem = 'This field is required.';
                } else if (rule[0] === 'email' && !emailPattern.test(value)) {
                    problem = rule[2];
                } else if (rule[1] > 0 && value.length < rule[1]) {
                    problem = rule[2];
                } else if (rule[0] === 'message' && value.length > 2000) {
                    problem = 'Message must not exceed 2000 characters.';
                }

                if (problem) {
                    setError(field, problem);
                    valid = false;
                }
            });

            return valid;
        }

        // Live clearing of the error as soon as the user types again
        form.querySelectorAll('.form-control').forEach(function (field) {
            field.addEventListener('input', function () { clearError(field); });
        });

        form.addEventListener('submit', function (event) {
            event.preventDefault();

            if (!validate()) {
                showToast('Please correct the highlighted fields.', 'error');
                var firstBad = form.querySelector('.is-invalid');
                if (firstBad) firstBad.focus();
                return;
            }

            // Loading state on the button
            var originalHtml = submitButton ? submitButton.innerHTML : '';
            if (submitButton) {
                submitButton.disabled = true;
                submitButton.innerHTML =
                    '<span class="spinner-border spinner-border-sm"></span> Sending...';
            }

            var data = new FormData(form);

            fetch(form.getAttribute('data-action'), {
                method: 'POST',
                body: data,
                headers: { 'Accept': 'application/json' }
            })
            .then(function (response) { return response.json(); })
            .then(function (result) {
                if (result.success) {
                    showToast(result.message, 'success');
                    form.reset();
                } else {
                    showToast(result.message || 'Could not send the message.', 'error');
                }
            })
            .catch(function () {
                // Network problem or non-JSON response: fall back to a normal
                // form submission so the message is still delivered.
                showToast('Sending normally, please wait...', 'info');
                form.submit();
            })
            .finally(function () {
                if (submitButton) {
                    submitButton.disabled = false;
                    submitButton.innerHTML = originalHtml;
                }
            });
        });
    }

    /* ======================================================================
       11. ADMIN EXTRAS
       ====================================================================== */

    /** Sidebar drawer on small screens. */
    function initAdminSidebar() {
        var sidebar = document.getElementById('adminSidebar');
        var toggle = document.getElementById('sidebarToggle');
        var backdrop = document.getElementById('sidebarBackdrop');
        if (!sidebar) return;

        function setOpen(open) {
            sidebar.classList.toggle('open', open);
            if (backdrop) backdrop.classList.toggle('show', open);
        }

        if (toggle) toggle.addEventListener('click', function () {
            setOpen(!sidebar.classList.contains('open'));
        });
        if (backdrop) backdrop.addEventListener('click', function () { setOpen(false); });
    }

    /** Tabs on the settings page. */
    function initTabs() {
        var buttons = document.querySelectorAll('.tab-btn[data-tab]');
        if (buttons.length === 0) return;

        function activate(name) {
            buttons.forEach(function (b) {
                b.classList.toggle('active', b.getAttribute('data-tab') === name);
            });
            document.querySelectorAll('.tab-pane').forEach(function (pane) {
                pane.classList.toggle('active', pane.id === 'tab-' + name);
            });
        }

        buttons.forEach(function (button) {
            button.addEventListener('click', function () {
                activate(button.getAttribute('data-tab'));
            });
        });

        // The controller can request a tab, e.g. after a password error
        var preset = document.body.getAttribute('data-tab');
        if (preset) activate(preset);
    }

    /** Proficiency range slider -> live numeric label. */
    function initRangeLabels() {
        document.querySelectorAll('input[type="range"][data-output]').forEach(function (input) {
            var output = document.getElementById(input.getAttribute('data-output'));
            if (!output) return;
            function sync() { output.textContent = input.value + '%'; }
            input.addEventListener('input', sync);
            sync();
        });
    }

    /** Character counter for textareas with data-maxlength. */
    function initCharCounters() {
        document.querySelectorAll('textarea[data-maxlength]').forEach(function (area) {
            var max = parseInt(area.getAttribute('data-maxlength'), 10);
            var counter = document.createElement('div');
            counter.className = 'form-text';
            area.parentNode.appendChild(counter);

            function sync() {
                counter.textContent = area.value.length + ' / ' + max + ' characters';
            }
            area.addEventListener('input', sync);
            sync();
        });
    }

    /* ======================================================================
       BOOT
       ====================================================================== */
    document.addEventListener('DOMContentLoaded', function () {
        initTheme();
        initNavbar();
        initTyping();
        initReveal();
        initSkillBars();
        initProjectFilter();
        initAlertToasts();
        initConfirmDialogs();
        initBackToTop();
        initContactForm();
        initAdminSidebar();
        initTabs();
        initRangeLabels();
        initCharCounters();
    });
})();

```

---
