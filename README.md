```mermaid
classDiagram
    class Title {
        +name: str
        +release_year: int
        +seasons: list
        +reviews: list
        +play_media()
    }
    class Film {
        +length_minutes: int
    }
    class TVShow {
        +seasons_count: int
    }
    class Season {
        +season_number: int
        +episodes: list
    }
    class Episode {
        +episode_title: str
        +duration_seconds: int
    }
    class Review {
        +rating_stars: int
        +review_text: str
    }
    class Actor {
        +full_name: str
    }
    class Genre {
        +genre_name: str
        +get_media_catalog()
    }
    Title <|-- Film
    Title <|-- TVShow
    Title *-- Season
    Title *-- Review
    Season *-- Episode
