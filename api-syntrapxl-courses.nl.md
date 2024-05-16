---
postUuid: 3f30a48e-8775-43f5-b63c-bee77751e0fe
title: API SyntraPXL Opleidingen
slug: api-syntrapxl-opleidingen
tags:
  - Databases
categories:
  - Backend
---

Maak kennis met de API van SyntraPXL Opleidingen. Deze API biedt een dataset aan waarin gegevens rondom opleidingen van SyntraPXL zijn opgenomen. De API kan gebruikt worden via een `Personal Access Token` van Code Coaching.

## Personal Access Token

Om deze oefening te kunnen maken heb je een personal access token nodig. Deze kun je genereren via jouw [profiel](https://code-coaching.dev/profiel). Na het genereren krijg je deze één keer te zien, bijv. `69|U4Kpv9yZkl4Y92J9onqAoSe7EIyKzhKyWEnv0OIt96cef6b1`. Ben je deze kwijt? Dan kun je een nieuwe genereren.

Het is belangrijk dat je deze token privé houdt. De token geeft je toegang tot jouw account en kan gebruikt worden om allerlei acties uit te voeren. Indien je Git gebruikt, zorg er dan voor dat je de token **NIET** commit.

Deze access token zal je als `Bearer Token` moeten meesturen met elke api call. Indien je een opfrissing nodig hebt, kan je de blogpost [CRUD Oefening](https://code-coaching.dev/blogs/crud-oefening) raadplegen.

## Endpoints

### Alle opleidingen

https://code-coaching.dev/api/syntrapxl/courses

Dit geeft een response terug met volgende structuur.

`courses`: dit bevat een `pagination` object, dit bevat enkele properties die je kan gebruiken om te navigeren door de lijst van opleidingen op basis van URL's. De `data` property bevat een array van opleidingen.

Alle andere properties op hetzelfde niveau als `courses` zijn lijsten van verschillende soorten data die je kan gebruiken om de opleidingen te filteren.

```json
{
  "courses": {
    "current_page": 1,
    "data": [
      {
        "id": 1,
        "url": "https://www.syntrapxl.be/opleidingen/3d-bouwkundig-tekenen-revit-kort",
        "title": "3D Bouwkundig tekenen in Revit - kort",
        "teaser": "Ben je klaar om je eerste professionele stappen in 3D-tekenen voor BIM en architectuur te zetten? Wil je je bijscholen en van Autocad (of een andere 2D tekenprogramma) upgraden naar 3D plantekenen in de industriestandaard Revit? Ben je nieuwsgierig naar hoe de digitale toekomst van de bouw uitziet? Dan ben je op het SyntraPXL expertisecentrum van BIM op je plaats.",
        "price_excl": 805.79,
        "price_incl": 975,
        "image": "https://www.syntrapxl.be/sites/default/files/colli/autocad-en-inventor.jpg",
        "is_business": 0,
        "program_text": "<p>• Introductie + user interface<br>• Basisinstellingen <br>• Grids <br>• Components (muren/vloeren/deuren en ramen/binnenschrijnwerk/curtain walls/mullions/structural) <br>• Stairs en railings <br>• Roofs en ceilings (footprint roof, extruded roof, details en aansluitingen, dakramen, dakgoot, ceiling) <br>• Begrippen category/ Family/Type/Instance… <br>• Project views: Grondplannen/Zichten/Sneden/Legendes/3D… <br>• Visibility + grafic display <br>• Manipulatie van views <br>• Bladopmaak/Printen, plotten in revit <br>• Exporteren van bestanden</p>\n",
        "kmo_theme_id": 1,
        "sector_id": 1,
        "course_type_id": 1,
        "duration_id": 1,
        "level_id": null,
        "study_type_id": null,
        "details_text": "<p>Architecten, ingenieurs, tekenaars en andere professionals gebruiken REVIT voor het maken, weergeven, beheren, uitzetten, delen en opnieuw gebruiken van nauwkeurige, zeer gedetailleerde tekeningen. Het bouwproces van de toekomst kan niet meer zonder goede BIM-tekenaars. Met deze avondcursus leer je basisprincipes van hoe je een 3D-model opbouwt en omzet in leesbare plannen met de razend populaire REVIT-software.</p>\n",
        "details_extra_info": "<p>BYOD (Bring Your Own Device): om optimaal thuis en op de campus te kunnen werken, breng je je eigen laptop mee. <a href=\"https://syntracloud.be/syntrapxl/pdf/BIM_laptop_vereisten.pdf\" target=\"_blank\">Download hier de infofiche met alle technische voorwaarden waaraan je toestel moet voldoe</a>n.</p>\n",
        "details_for_text": "<p>Architecten, ingenieurs, tekenaars, ontwerpers en andere professionals die Revit willen gebruiken voor het maken, weergeven, beheren, uitzetten, delen en opnieuw gebruiken van nauwkeurige, gedetailleerde 3D-plannen.<br>Je werkt volledig digitaal, dus een degelijke pc-vaardigheid (vlot kunnen werken met Windows, Word en Excel) is vereist. We beginnen van nul, maar je hebt best wat voeling of lichte ervaring met 3D (bv met Sketch-up).<br>Een gezonde interesse in de bouwwereld en bouwtechniek helpt je snel op weg.<br>Je kan vlot met computer en muis werken, en je hebt aanleg voor grafisch werk en tekenen.</p>\n",
        "details_requirements_text": null,
        "created_at": "2024-05-02T19:08:53.000000Z",
        "updated_at": "2024-05-02T19:08:53.000000Z",
        "savings": [
          {
            "id": 1,
            "name": "kmo",
            "created_at": "2024-05-02T19:05:20.000000Z",
            "updated_at": "2024-05-02T19:05:20.000000Z",
            "pivot": {
              "course_id": 1,
              "saving_id": 1
            }
          }
        ],
        "special_properties": [],
        "price_details": [],
        "people": [
          {
            "id": 1,
            "name": "Jos Cielen",
            "image": "https://www.syntrapxl.be/sites/default/files/styles/employee_large/public/Jos-Cielen_0.jpg?itok=SBgsIpeV",
            "is_teacher": 0,
            "is_business_developer": 1,
            "created_at": "2024-05-02T19:08:53.000000Z",
            "updated_at": "2024-05-02T19:08:53.000000Z",
            "pivot": {
              "course_id": 1,
              "person_id": 1
            }
          }
        ],
        "kmo_theme": {
          "id": 1,
          "name": "Digitalisering - Software",
          "created_at": "2024-05-02T19:08:53.000000Z",
          "updated_at": "2024-05-02T19:08:53.000000Z"
        },
        "sector": {
          "id": 1,
          "name": "CAD/CAM en 3D",
          "created_at": "2024-05-02T19:08:53.000000Z",
          "updated_at": "2024-05-02T19:08:53.000000Z"
        },
        "course_type": {
          "id": 1,
          "name": "Kortlopende opleidingen",
          "created_at": "2024-05-02T19:08:53.000000Z",
          "updated_at": "2024-05-02T19:08:53.000000Z"
        },
        "duration": {
          "id": 1,
          "name": "10 sessies",
          "created_at": "2024-05-02T19:08:53.000000Z",
          "updated_at": "2024-05-02T19:08:53.000000Z"
        },
        "level": null,
        "study_type": null
      }
      // ...
    ],
    "first_page_url": "https://code-coaching.dev/api/syntrapxl/courses?page=1",
    "from": 1,
    "last_page": 75,
    "last_page_url": "https://code-coaching.dev/api/syntrapxl/courses?page=75",
    "links": [
      {
        "url": null,
        "label": "&laquo; Vorige",
        "active": false
      },
      {
        "url": "https://code-coaching.dev/api/syntrapxl/courses?page=1",
        "label": "1",
        "active": true
      },
      {
        "url": "https://code-coaching.dev/api/syntrapxl/courses?page=2",
        "label": "2",
        "active": false
      },
      {
        "url": "https://code-coaching.dev/api/syntrapxl/courses?page=3",
        "label": "3",
        "active": false
      },
      {
        "url": "https://code-coaching.dev/api/syntrapxl/courses?page=4",
        "label": "4",
        "active": false
      },
      {
        "url": "https://code-coaching.dev/api/syntrapxl/courses?page=5",
        "label": "5",
        "active": false
      },
      {
        "url": "https://code-coaching.dev/api/syntrapxl/courses?page=6",
        "label": "6",
        "active": false
      },
      {
        "url": "https://code-coaching.dev/api/syntrapxl/courses?page=7",
        "label": "7",
        "active": false
      },
      {
        "url": "https://code-coaching.dev/api/syntrapxl/courses?page=8",
        "label": "8",
        "active": false
      },
      {
        "url": "https://code-coaching.dev/api/syntrapxl/courses?page=9",
        "label": "9",
        "active": false
      },
      {
        "url": "https://code-coaching.dev/api/syntrapxl/courses?page=10",
        "label": "10",
        "active": false
      },
      {
        "url": null,
        "label": "...",
        "active": false
      },
      {
        "url": "https://code-coaching.dev/api/syntrapxl/courses?page=74",
        "label": "74",
        "active": false
      },
      {
        "url": "https://code-coaching.dev/api/syntrapxl/courses?page=75",
        "label": "75",
        "active": false
      },
      {
        "url": "https://code-coaching.dev/api/syntrapxl/courses?page=2",
        "label": "Volgende &raquo;",
        "active": false
      }
    ],
    "next_page_url": "https://code-coaching.dev/api/syntrapxl/courses?page=2",
    "path": "https://code-coaching.dev/api/syntrapxl/courses",
    "per_page": 10,
    "prev_page_url": null,
    "to": 10,
    "total": 746
  },
  "sectors": [
    {
      "id": 1,
      "name": "CAD/CAM en 3D",
      "created_at": "2024-05-02T19:08:53.000000Z",
      "updated_at": "2024-05-02T19:08:53.000000Z",
      "courses_count": 14
    }
    // ...
  ],
  "start_dates": [
    {
      "name": "mei 2024",
      "timestamp": 1714521600,
      "count": 36
    }
    // ...
  ],
  "course_types": [
    {
      "id": 1,
      "name": "Kortlopende opleidingen",
      "created_at": "2024-05-02T19:08:53.000000Z",
      "updated_at": "2024-05-02T19:08:53.000000Z",
      "courses_count": 430
    }
    // ...
  ],
  "durations": [
    {
      "id": 1,
      "name": "10 sessies",
      "created_at": "2024-05-02T19:08:53.000000Z",
      "updated_at": "2024-05-02T19:08:53.000000Z",
      "courses_count": 13
    }
    // ...
  ],
  "locations": [
    {
      "id": 1,
      "name": "Pelt",
      "created_at": "2024-05-02T19:08:53.000000Z",
      "updated_at": "2024-05-02T19:08:53.000000Z",
      "start_dates_count": 101
    }
    // ...
  ],
  "savings": [
    {
      "id": 1,
      "name": "kmo",
      "created_at": "2024-05-02T19:05:20.000000Z",
      "updated_at": "2024-05-02T19:05:20.000000Z",
      "courses_count": 312
    }
    // ...
  ],
  "special_properties": [
    {
      "id": 1,
      "name": "In de kijker",
      "created_at": "2024-05-02T19:08:53.000000Z",
      "updated_at": "2024-05-02T19:08:53.000000Z",
      "courses_count": 100
    }
    // ...
  ],
  "levels": [
    {
      "id": 1,
      "name": "Beginner",
      "created_at": "2024-05-02T19:08:58.000000Z",
      "updated_at": "2024-05-02T19:08:58.000000Z",
      "courses_count": 62
    }
    // ...
  ],
  "study_types": [
    {
      "id": 1,
      "name": "Hybride leren",
      "created_at": "2024-05-02T19:08:53.000000Z",
      "updated_at": "2024-05-02T19:08:53.000000Z",
      "courses_count": 15
    }
    // ...
  ]
}
```

## Specifieke opleiding

https://code-coaching.dev/api/syntrapxl/courses/{id} waarbij `{id}` het id van de opleiding is, bijvoorbeeld: https://code-coaching.dev/api/syntrapxl/courses/1

Dit geeft een object terug met de details van een opleiding.

```json
{
  "id": 1,
  "url": "https://www.syntrapxl.be/opleidingen/3d-bouwkundig-tekenen-revit-kort",
  "title": "3D Bouwkundig tekenen in Revit - kort",
  "teaser": "Ben je klaar om je eerste professionele stappen in 3D-tekenen voor BIM en architectuur te zetten? Wil je je bijscholen en van Autocad (of een andere 2D tekenprogramma) upgraden naar 3D plantekenen in de industriestandaard Revit? Ben je nieuwsgierig naar hoe de digitale toekomst van de bouw uitziet? Dan ben je op het SyntraPXL expertisecentrum van BIM op je plaats.",
  "price_excl": 805.79,
  "price_incl": 975,
  "image": "https://www.syntrapxl.be/sites/default/files/colli/autocad-en-inventor.jpg",
  "is_business": 0,
  "program_text": "<p>• Introductie + user interface<br>• Basisinstellingen <br>• Grids <br>• Components (muren/vloeren/deuren en ramen/binnenschrijnwerk/curtain walls/mullions/structural) <br>• Stairs en railings <br>• Roofs en ceilings (footprint roof, extruded roof, details en aansluitingen, dakramen, dakgoot, ceiling) <br>• Begrippen category/ Family/Type/Instance… <br>• Project views: Grondplannen/Zichten/Sneden/Legendes/3D… <br>• Visibility + grafic display <br>• Manipulatie van views <br>• Bladopmaak/Printen, plotten in revit <br>• Exporteren van bestanden</p>\n",
  "kmo_theme_id": 1,
  "sector_id": 1,
  "course_type_id": 1,
  "duration_id": 1,
  "level_id": null,
  "study_type_id": null,
  "details_text": "<p>Architecten, ingenieurs, tekenaars en andere professionals gebruiken REVIT voor het maken, weergeven, beheren, uitzetten, delen en opnieuw gebruiken van nauwkeurige, zeer gedetailleerde tekeningen. Het bouwproces van de toekomst kan niet meer zonder goede BIM-tekenaars. Met deze avondcursus leer je basisprincipes van hoe je een 3D-model opbouwt en omzet in leesbare plannen met de razend populaire REVIT-software.</p>\n",
  "details_extra_info": "<p>BYOD (Bring Your Own Device): om optimaal thuis en op de campus te kunnen werken, breng je je eigen laptop mee. <a href=\"https://syntracloud.be/syntrapxl/pdf/BIM_laptop_vereisten.pdf\" target=\"_blank\">Download hier de infofiche met alle technische voorwaarden waaraan je toestel moet voldoe</a>n.</p>\n",
  "details_for_text": "<p>Architecten, ingenieurs, tekenaars, ontwerpers en andere professionals die Revit willen gebruiken voor het maken, weergeven, beheren, uitzetten, delen en opnieuw gebruiken van nauwkeurige, gedetailleerde 3D-plannen.<br>Je werkt volledig digitaal, dus een degelijke pc-vaardigheid (vlot kunnen werken met Windows, Word en Excel) is vereist. We beginnen van nul, maar je hebt best wat voeling of lichte ervaring met 3D (bv met Sketch-up).<br>Een gezonde interesse in de bouwwereld en bouwtechniek helpt je snel op weg.<br>Je kan vlot met computer en muis werken, en je hebt aanleg voor grafisch werk en tekenen.</p>\n",
  "details_requirements_text": null,
  "created_at": "2024-05-02T19:08:53.000000Z",
  "updated_at": "2024-05-02T19:08:53.000000Z",
  "savings": [
    {
      "id": 1,
      "name": "kmo",
      "created_at": "2024-05-02T19:05:20.000000Z",
      "updated_at": "2024-05-02T19:05:20.000000Z",
      "pivot": {
        "course_id": 1,
        "saving_id": 1
      }
    }
  ],
  "special_properties": [],
  "price_details": [],
  "people": [
    {
      "id": 1,
      "name": "Jos Cielen",
      "image": "https://www.syntrapxl.be/sites/default/files/styles/employee_large/public/Jos-Cielen_0.jpg?itok=SBgsIpeV",
      "is_teacher": 0,
      "is_business_developer": 1,
      "created_at": "2024-05-02T19:08:53.000000Z",
      "updated_at": "2024-05-02T19:08:53.000000Z",
      "pivot": {
        "course_id": 1,
        "person_id": 1
      }
    }
  ],
  "kmo_theme": {
    "id": 1,
    "name": "Digitalisering - Software",
    "created_at": "2024-05-02T19:08:53.000000Z",
    "updated_at": "2024-05-02T19:08:53.000000Z"
  },
  "sector": {
    "id": 1,
    "name": "CAD/CAM en 3D",
    "created_at": "2024-05-02T19:08:53.000000Z",
    "updated_at": "2024-05-02T19:08:53.000000Z"
  },
  "course_type": {
    "id": 1,
    "name": "Kortlopende opleidingen",
    "created_at": "2024-05-02T19:08:53.000000Z",
    "updated_at": "2024-05-02T19:08:53.000000Z"
  },
  "duration": {
    "id": 1,
    "name": "10 sessies",
    "created_at": "2024-05-02T19:08:53.000000Z",
    "updated_at": "2024-05-02T19:08:53.000000Z"
  },
  "level": null,
  "study_type": null,
  "start_dates": [
    {
      "id": 1,
      "course_id": 1,
      "date": "2024-10-02 19:00:00",
      "day_id": 1,
      "location_id": 1,
      "available_spaces": 1,
      "created_at": "2024-05-02T19:08:53.000000Z",
      "updated_at": "2024-05-02T19:08:53.000000Z"
    }
  ]
}
```

Merk op dat alle data mogelijks `null` kan zijn. Dit betekent dat je hiermee rekening moet houden in je frontend.
