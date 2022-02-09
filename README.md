# luigi_demo
demo / tutorial of python and luigi

Luigi should run all the Tasks in the schedule (this should go relatively quickly). You can then access the Central Scheduler at the following address: http://localhost:8082, and you should see the list of Task that have been run at that moment, along with their status.
##  Docs
- https://kapernikov.com/using-luigi-to-power-a-reporting-pipeline/
- https://blog.junaideffendi.com/2018/06/luigi-data-pipelines-for-batch-processing.html

## Run

- python le_main.py

##  Run with luigi

pip install luigi

 src/luigi/jobs.py

```
luigi –m <path to scheduler/job> <scheduler/job class name> --param1 <param1> ….. --paramN <paramN>
  
luigi –m luigi.jobs MyJob --name Junaid
```

 ```
import luigi
class MyJob(luigi.Task):
            name = luigi.Parameter(default=None)
            def requires(self):
                        return depends()
            def run(self):
                        doWork()
            def input(self):
                        return <input path>
            def output(self):
                        return <output path>
```
