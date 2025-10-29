# Feature 26: Todoist Integration

**Epic:** [05-external-app-integrations](../epics/05-external-app-integrations.md)
**Status:** Not Started
**Priority:** High
**Estimated Effort:** M
**Assigned To:** TBD
**Dependencies:** [29-unified-task-suggestion-inbox](29-unified-task-suggestion-inbox.md)

## Description

Create seamless integration with Todoist that allows intelligent task import suggestions while preserving the bullet journal philosophy of intentional task selection. This eliminates the manual copying process currently required in the user's workflow.

## User Stories

### Primary User Story
**As a** Todoist and bullet journal user
**I want** relevant Todoist tasks to appear as suggestions in my daily planning
**So that** I can eliminate manual copying while maintaining intentional task selection

### Additional User Stories
1. **As a** busy person, **I want** smart filtering of Todoist tasks, **so that** I only see relevant items for today's planning
2. **As a** project manager, **I want** task context preserved during import, **so that** project information isn't lost
3. **As a** completion tracker, **I want** completed tasks to optionally sync back to Todoist, **so that** my systems stay synchronized
4. **As a** privacy-conscious user, **I want** control over what data is accessed, **so that** I maintain security

## Acceptance Criteria

- [ ] OAuth integration with Todoist API for secure authentication
- [ ] Smart task filtering based on due dates, priorities, and user patterns
- [ ] Task suggestion interface showing Todoist tasks for consideration
- [ ] One-click import of selected tasks with context preservation
- [ ] Bidirectional sync option for task completion status
- [ ] Project and label information maintained during import
- [ ] Batch import capabilities for multiple task selection
- [ ] Integration status monitoring and error handling

## Technical Details

### Integration Architecture
```javascript
TodoistIntegration {
  userId: string,
  todoistAccessToken: string,
  syncSettings: {
    autoSuggestTodayTasks: boolean,
    autoSuggestOverdueTasks: boolean,
    syncCompletions: boolean,
    includeProjects: string[],
    excludeLabels: string[]
  },
  lastSyncDate: Date,
  isActive: boolean
}

TodoistTask {
  todoistId: string,
  content: string,
  description: string,
  dueDate?: Date,
  priority: number,
  projectName: string,
  labels: string[],
  suggestedForDate: Date,
  importStatus: 'suggested' | 'imported' | 'dismissed'
}
```

### APIs/Endpoints
```
POST /api/integrations/todoist/connect - Establish Todoist connection
GET /api/integrations/todoist/tasks - Get filtered Todoist tasks
POST /api/integrations/todoist/import - Import selected tasks
PUT /api/integrations/todoist/sync - Sync completion status back
DELETE /api/integrations/todoist/disconnect - Remove integration
```

## Definition of Done

- [ ] Todoist OAuth integration working securely
- [ ] Task filtering and suggestion system operational
- [ ] Import workflow functional with context preservation
- [ ] Bidirectional sync working for completions
- [ ] Error handling and reconnection logic implemented