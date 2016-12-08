- First run

mapper containers=2
reducer containers=2
container.memory=512
mapper JVM heap=409
reducer JVM heap=409

teragen duration:
real    0m19.516s

terasort duration:
real    0m29.166s


- Second run

mapper containers=2
reducer containers=2
container.memory=1024
mapper JVM heap=819
reducer JVM heap=819

teragen duration:
real    0m19.622s

terasort duration:
real    0m29.260s


- Third run

mapper containers=4
reducer containers=4
container.memory=1536
mapper JVM heap=1228
reducer JVM heap=1228

teragen duration:
real    0m18.562s

terasort duration:
real    0m29.336s


- Fourth run

mapper containers=4
reducer containers=4
container.memory=3072
mapper JVM heap=2457
reducer JVM heap=2457

teragen duration:
real    0m21.550s

terasort duration:
real    0m36.168s