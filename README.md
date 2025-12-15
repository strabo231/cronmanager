# CronManager - User-Friendly Cron Job Management

Finally, a cron interface that doesn't make you want to pull your hair out! CronManager brings modern, intuitive management to cron jobs.

## Why CronManager?

**The Problem:** `crontab -e` is cryptic, error-prone, and intimidating  
**The Solution:** CronManager makes cron jobs easy

- 📋 **Clear listing** - See all jobs numbered and formatted nicely
- ➕ **Easy adding** - Guided prompts, no syntax memorization
- ✏️ **Simple editing** - Modify jobs by number
- ❌ **Quick removal** - Delete jobs without opening an editor
- 🔍 **Validation** - Check if schedules are valid before adding
- ⏰ **Next run times** - See when jobs will execute next
- 🔄 **Enable/Disable** - Turn jobs on/off without deleting
- 💾 **Backup/Restore** - Save and restore your crontab

## Installation

```bash
curl -sSL https://raw.githubusercontent.com/YOUR_USERNAME/cronmanager/main/install.sh | bash
```

## Quick Start

```bash
# List all jobs
cronman list

# Add a new job (interactive)
cronman add

# Remove job #3
cronman remove 3

# Disable job #2 temporarily
cronman disable 2

# See common examples
cronman examples
```

## Commands

```
list, ls              List all cron jobs
add                   Add a new cron job (interactive)
remove, rm <n>        Remove cron job by number
disable <n>           Disable a job (comments it out)
enable <n>            Enable a disabled job
validate <schedule>   Check if schedule is valid
next <schedule>       Show next run time
examples              Show common schedules
backup                Save current crontab
restore <file>        Restore from backup
clear                 Remove all jobs (careful!)
```

## Common Schedules

| When | Schedule | Shorthand |
|------|----------|-----------|
| Every hour | `0 * * * *` | `@hourly` |
| Daily at 2 AM | `0 2 * * *` | `@daily` |
| Every Sunday | `0 0 * * 0` | `@weekly` |
| 1st of month | `0 0 1 * *` | `@monthly` |
| Weekdays 9 AM | `0 9 * * 1-5` | - |
| Every 15 min | `*/15 * * * *` | - |
| At boot | `@reboot` | `@reboot` |

## Why Better Than `crontab -e`?

| Feature | crontab -e | CronManager |
|---------|-----------|-------------|
| Easy to use | ❌ | ✅ |
| See job numbers | ❌ | ✅ |
| Validate syntax | ❌ | ✅ |
| Show next run | ❌ | ✅ |
| Descriptions | ❌ | ✅ |
| Disable/enable | ❌ | ✅ |
| Interactive | ❌ | ✅ |
| Backup/restore | ❌ | ✅ |

## Examples

**Daily backup:**
```bash
cronman add
# Description: Daily backup
# Schedule: @daily
# Command: /home/user/backup.sh
```

**Clean logs weekly:**
```bash
cronman add
# Schedule: @weekly
# Command: find /var/log -name "*.log" -mtime +30 -delete
```

**Temporarily stop a job:**
```bash
cronman disable 3    # Pause it
cronman enable 3     # Resume later
```

## License

MIT License - see [LICENSE](LICENSE)

## Author

Sean - [@strabo231](https://github.com/strabo231)
