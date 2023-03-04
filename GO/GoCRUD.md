# Create Read Update Delete
## A method to transmit changes to a database

    Create – Uses the HTTP POST method to add one or more records.
    Read – Uses the HTTP GET method to retrieve one or more records * that match certain criteria.
    Update – Uses the HTTP PUT or PATCH methods to update a record.
    Delete – Uses the HTTP DELETE method to remove one or more records.

## GORM 
is a fantastic object-relational mapper (ORM) library for Golang that claims to help developers build faster and make fewer errors.

The GORM library is built on top of the Golang database/sql package. That means it only works with relational databases (MySQL, PostgreSQL, SQLite, etc). Like other ORMs, GORM also provides a lot of tools to help developers interact with databases with ease.

    package models

    import (
        "time"

        "github.com/google/uuid"
    )

    type Post struct {
        ID        uuid.UUID `gorm:"type:uuid;default:uuid_generate_v4();primary_key" json:"id,omitempty"`
        Title     string    `gorm:"uniqueIndex;not null" json:"title,omitempty"`
        Content   string    `gorm:"not null" json:"content,omitempty"`
        Image     string    `gorm:"not null" json:"image,omitempty"`
        User      uuid.UUID `gorm:"not null" json:"user,omitempty"`
        CreatedAt time.Time `gorm:"not null" json:"created_at,omitempty"`
        UpdatedAt time.Time `gorm:"not null" json:"updated_at,omitempty"`
    }

    type CreatePostRequest struct {
        Title     string    `json:"title"  binding:"required"`
        Content   string    `json:"content" binding:"required"`
        Image     string    `json:"image" binding:"required"`
        User      string    `json:"user,omitempty"`
        CreatedAt time.Time `json:"created_at,omitempty"`
        UpdatedAt time.Time `json:"updated_at,omitempty"`
    }

    type UpdatePost struct {
        Title     string    `json:"title,omitempty"`
        Content   string    `json:"content,omitempty"`
        Image     string    `json:"image,omitempty"`
        User      string    `json:"user,omitempty"`
        CreateAt  time.Time `json:"created_at,omitempty"`
        UpdatedAt time.Time `json:"updated_at,omitempty"`
    }

