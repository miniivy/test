podTemplate(
    label: 'mypod',
    volumes: [
        emptyDirVolume(mountPath: '/etc/gitrepo', memory: false),
        hostPathVolume(mountPath: '/var/run/docker.sock', hostPath: '/var/run/docker.sock')
    ],
    containers:
    [
        containerTemplate(name: 'git', image: 'alpine/git', ttyEnabled: true, command: 'cat'),
        containerTemplate(name: 'python', image: 'python:3.7.2', command: 'cat', ttyEnabled: true),
        containerTemplate(name: 'docker', image: 'docker', command: 'cat', ttyEnabled: true,
            envVars: [secretEnvVar(key: 'DOCKER_HUB_PASSWORD', secretName: 'docker-hub-password', secretKey: 'DOCKER_HUB_PASSWORD')]
        )
    ]
)
