# Feature 29: Unified Task Suggestion Inbox

**Epic:** [05-external-app-integrations](../epics/05-external-app-integrations.md)
**Status:** Not Started
**Priority:** High
**Estimated Effort:** M
**Assigned To:** TBD
**Dependencies:** [02-rapid-logging-interface](02-rapid-logging-interface.md)

## Description

Create centralized inbox that aggregates task suggestions from all integrated sources (Todoist, messaging apps, email, calendar) and presents them in a unified interface for user review and selection. This is the core feature that eliminates task fragmentation.

## User Stories

### Primary User Story
**As a** multi-platform task user
**I want** all my task suggestions in one place
**So that** I can efficiently review and select what to include in my daily bullet journal

### Additional User Stories
1. **As a** efficient planner, **I want** smart categorization of suggestions, **so that** I can quickly process different types of tasks
2. **As a** busy person, **I want** bulk actions for suggestions, **so that** I can quickly accept or dismiss multiple items
3. **As a** context switcher, **I want** source indicators, **so that** I know where each suggestion came from
4. **As a** learning user, **I want** the system to learn my preferences, **so that** better suggestions appear over time

## Acceptance Criteria

- [ ] Unified inbox displaying suggestions from all connected integrations
- [ ] Smart categorization (work, personal, urgent, routine) with visual indicators
- [ ] Bulk selection capabilities for efficient processing
- [ ] Source attribution showing where each suggestion originated
- [ ] Priority scoring based on multiple factors (due date, source importance, user patterns)
- [ ] Quick actions: accept, dismiss, reschedule, modify
- [ ] Search and filtering within suggestions
- [ ] Learning system that improves suggestion relevance over time

## Technical Details

### Unified Inbox Architecture
```javascript
TaskSuggestion {
  id: string,
  userId: string,
  content: string,
  source: 'todoist' | 'whatsapp' | 'email' | 'calendar' | 'ai_generated',
  sourceId: string,
  category: 'work' | 'personal' | 'urgent' | 'routine' | 'goal_related',
  priority: number,
  suggestedDate: Date,
  dueDate?: Date,
  context: object,
  status: 'pending' | 'accepted' | 'dismissed' | 'rescheduled',
  createdAt: Date,
  processedAt?: Date
}

InboxSession {
  id: string,
  userId: string,
  date: Date,
  suggestionsProcessed: number,
  acceptanceRate: number,
  timeSpent: number,
  patterns: object
}
```

### APIs/Endpoints
```
GET /api/inbox/suggestions - Get current task suggestions
POST /api/inbox/process - Process bulk suggestion actions
PUT /api/inbox/suggestion/{id} - Update individual suggestion
GET /api/inbox/stats - Get inbox processing statistics
POST /api/inbox/learn - Submit learning feedback
```

## Definition of Done

- [ ] Unified inbox interface implemented with all integrations
- [ ] Bulk processing capabilities functional
- [ ] Smart categorization working accurately
- [ ] Learning system operational and improving suggestions
- [ ] Performance optimized for large suggestion volumes