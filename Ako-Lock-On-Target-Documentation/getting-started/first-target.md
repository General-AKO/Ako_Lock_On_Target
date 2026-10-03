# Your First Target

This walkthrough creates a simple target suitable for a standard enemy.

## 1. Add the Lock-On Target component

Add the plugin's target component to the Actor Blueprint that should be available to the lock-on system.

## 2. Choose a target point

For a first setup, keep the target point on **Default**. This avoids introducing bone-specific behavior until the basic configuration works.

## 3. Set the default icon

Assign **Lock On Icon** and adjust **Custom Target Icon Size** as needed.

The default icon can also serve as a fallback for bones that do not have a dedicated icon.

## 4. Create a Target UI Data Asset

Create a Target UI Data Asset and decide whether the target should use:

- **Custom Widget** for your own Widget Blueprint design, or
- **Status Widget** for the built-in status-oriented workflow.

## 5. Assign the Data Asset

Add the Data Asset to the target component's **UI Target Settings**.

## 6. Test in game

Your gameplay/lock-on Blueprint remains responsible for selecting the target and driving project-specific runtime values. Confirm that the target is selected and the expected UI appears.

Once this basic path works, continue with the configuration pages to add bone targeting, reusable status layouts, and world-space presentation.
