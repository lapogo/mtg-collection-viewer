# Testing

## Running Tests

Open `test/index.html` in a browser to run the complete test suite.

## Test Coverage (80+ tests)

- **Game Tracker** - Core state, life, damage, counters, mana, commander damage, mulligans, advanced mechanics
- **Card Back Visibility** - 3D flip effects, CSS transforms
- **Flavor Names** - Deck checker flavor name matching
- **Foil Shimmer** - Foil effect standardization
- **Copies Filter** - Oracle ID duplicate detection
- **Detail Page** - Card detail rendering, 3D effects
- **Trading Binder** - LocalStorage, share links, context menu

## Pre-Push Hook

The git pre-push hook automatically:
1. ✅ Validates JavaScript syntax for all files
2. ✅ Prevents broken code from being pushed
3. ✅ Reminds you to run browser tests

To manually check syntax:
```bash
node -c js/game-tracker.js
node -c test/test.js
```

## Test Organization

```
test/
├── index.html  # Test runner
└── test.js     # All test cases
```

All tests validate:
- State management correctness
- Game rule enforcement
- Edge case handling
- No regressions in core mechanics

Run tests before major changes to ensure nothing breaks!
