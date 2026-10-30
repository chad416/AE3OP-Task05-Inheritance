# AE3OP Task 05 - Inheritance

[Inheritance tutorial](https://github.com/icebeam7/oop-tutorials/blob/main/02-inheritance/README.md): a small turn-based dungeon minigame.

## Class hierarchy

```
Character            base class: Name, Health, MaxHealth, AttackPower, IsAlive,
 |                   protected constructor, virtual TakeDamage, virtual PerformAttack
 |-- Warrior         120 HP / 15 ATK, ShieldBlock: overrides TakeDamage and calls base.TakeDamage
 |-- Mage            80 HP / 25 ATK, Mana: Fireball costs 20 mana, weak staff hit (5) when out of mana
 |-- Goblin          60 HP / 10 ATK, 30 % chance of a second strike (Random.Shared)
 `-- Dragon          200 HP / 20 ATK boss, fire breath
```

## Steps done

1. Project setup: `InheritanceMinigame` console app with a `Classes` folder
2. `Character` base class
3. `Warrior` (`: base(...)`, `override`, `base.TakeDamage`)
4. `Mage`
5. `Dragon`
6. `Goblin`
7. Gameplay in `Program.cs`: the player is stored as a `Character` (Warrior or Mage) and all enemies sit in one `Queue<Character>`

## Run

```bash
dotnet run --project InheritanceMinigame
```
