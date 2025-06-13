# Changes introduced in the Constellation Modernization Assistant 1.0.8

Enhancements:
• Introduced the ability to store all modified rules in a dedicated branch during migration. This enables a new "branch development mode" within the migrated application, facilitating easier parallel development and review of changes.
• Enforced the requirement to lock application rulesets prior to initiating the migration process. This ensures data integrity and prevents unintended modifications during migration.

Bug Fixes:
• Resolved an issue that prevented installation on Oracle databases by limiting the size of the pyMessage column to 4000 characters.
• Fixed a bug where newly created rulesets were sometimes incorrectly added to the traditional application instead of the new one.
• Addressed a NullPointerException that was occasionally observed in the logs for the myStepPage within the pyc11BuildNewApp activity.
