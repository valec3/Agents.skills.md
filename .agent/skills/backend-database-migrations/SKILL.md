---
name: backend-database-migrations
description: Database versioning, migration best practices.
---

# Backend Database Migrations

## When to use this skill
- Database schema changes
- Version control for database
- Deploying schema updates
- Team collaboration

## Workflow
- [ ] Create migration files
- [ ] Write up() and down()
- [ ] Run migrations
- [ ] Track in version control
- [ ] Never edit existing migrations

## Instructions

### Create Migration
```bash
php spark make:migration add_users_table
```

### Migration File
```php
<?php

namespace App\Database\Migrations;

use CodeIgniter\Database\Migration;

class AddUsersTable extends Migration
{
    public function up()
    {
        $this->forge->addField([
            'id' => [
                'type' => 'INT',
                'constraint' => 11,
                'unsigned' => true,
                'auto_increment' => true
            ],
            'email' => [
                'type' => 'VARCHAR',
                'constraint' => 255,
                'unique' => true
            ],
            'created_at' => [
                'type' => 'DATETIME',
                'null' => true
            ]
        ]);
        $this->forge->addKey('id', true);
        $this->forge->createTable('users');
    }

    public function down()
    {
        $this->forge->dropTable('users');
    }
}
```

### Run Migrations
```bash
php spark migrate
php spark migrate:rollback
```

## Resources
- Always write down() method
- Test rollback
- Never modify existing migrations
