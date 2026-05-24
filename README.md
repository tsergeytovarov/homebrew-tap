# Homebrew Tap — tsergeytovarov

Личный Homebrew tap для приложений [Сергея Товарова](https://github.com/tsergeytovarov).

## Установка

```bash
brew tap tsergeytovarov/tap
```

Дальше — любая из формул ниже:

### ai-stats — Burn

macOS menu bar app для статистики использования AI-агентов и активности на GitHub.

```bash
brew install --cask ai-stats
```

Подробности: [tsergeytovarov/ai-stats](https://github.com/tsergeytovarov/ai-stats).

Обновление:

```bash
brew upgrade --cask ai-stats
```

Удаление со всеми данными (кроме Keychain):

```bash
brew uninstall --cask --zap ai-stats
```

Keychain-запись (`tech.popovs.aistats.github` — GitHub PAT) cask не зап'ит. Удалить вручную через **Keychain Access** → поиск `tech.popovs.aistats` → Delete.

## Что внутри tap'а

- `Casks/ai-stats.rb` — Burn (macOS menu bar AI-stats)

## Зачем отдельный репозиторий

Homebrew tap'ы по соглашению живут в репозиториях с префиксом `homebrew-`. Имя `homebrew-tap` маппится на короткое `tsergeytovarov/tap` при `brew tap`. Файлы Cask'ов лежат в `Casks/`, formulae — в `Formula/`.

## Обновление Cask

При новом релизе `ai-stats`:

1. Собрать DMG в основном репо: `./scripts/build-dmg.sh`
2. Создать GitHub release с DMG
3. В этом репо обновить `version` и `sha256` в `Casks/ai-stats.rb`, закоммитить и push'нуть

## Лицензия

MIT.
