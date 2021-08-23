# If you work on an HPC-cluster with Slurm, you will love these commands

# What you'll get

| Command name              | What it does                                                                                    | Example                                                          |
|---------------------------|-------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| `sq`                      | Short version for `squeue -u $USER`                                                             | ![Screenshot](sq.png?raw=true "sq")                              |
| `slurmlogpath $JOBID`     | Shows the path of the .out file from whereever you are                                          | ![Screenshot](slurmlogpath.png?raw=true "slurmlogpath")          |
| `ftails $JOBID`, `ftails` | Tails the job wherever you are. If no param is given, you'll see a screen with all running jobs | ![Screenshot](ftails.png?raw=true "ftails")                      |
| `rtest`                   | Creates a new, empty subfolder in the folder `~/test`                                           | ![Screenshot](rtest.png?raw=true "rtest")                        |
| `prettycsv $FILENAME`     | Prints a CSV in a prettier way                                                                  | ![Screenshot](prettycsv.png?raw=true "prettycsv")                |
| `mcd path`                | `cd`'s into a path and creates it if it doesn't exists                                          | ![Screenshot](mcd.png?raw=true "mcd")                            |
| `showmyjobsstatus`        | Shows my current job(s) status (required `whypending`)                                          | ![Screenshot](showmyjobsstatus.png?raw=true "showmyjobsstatus")  |
| `countdown $SEC`          | Shows a countdown for `$SEC` seconds                                                            | ![Screenshot](countdown.png?raw=true "countdown")                |
| `get_job_name $JOBID`     | Shows the name of the job `$JOBID`                                                              | ![Screenshot](get_job_name.png?raw=true "get_job_name")          |
| `slurminator`             | A whiptail GUI to handle slurm-jobs                                                             | ![Screenshot](slurminator.png?raw=true "slurminator")            |

# The installation is quite easy.

```
cp slurm_commands.sh ~/.slurm_commands.sh
echo "source ~/.slurm_commands.sh" >> "~/.$(basename $SHELL)rc"
```

# Dependencies

Only all the slurm-default-suite, perl and whiptail, and zsh/bash, which all should be installed on your system.
