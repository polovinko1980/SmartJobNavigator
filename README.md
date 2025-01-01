# Smart Job Navigator

An on-premises, Docker-based tool to search for LinkedIn job postings, track applications, and generate artifacts with the help of LLMs (Large Language Models).

## Dependencies

You will need to provide your own API key for OpenAI, which is used for generating artifacts such as job evaluations and adjusted resume files. 

To start the application, please run:

```bash
docker-compose up
```

Then navigate to the UI at:

```
http://localhost:8080/
```

The tool consists of three services, each wrapped in its own Docker container.

## Components

### [FrontEnd](https://github.com/polovinko1980/smart-job-navigator-frontend)

### [Dispatcher](https://github.com/polovinko1980/smart-job-navigator-dispatcher)

### [Scraper](https://github.com/polovinko1980/smart-job-navigator-scraper)

## Data Handling

The application is designed to run in a user-hosted and controlled environment, and thus it has no built-in security features.

All data is processed on-premises under the `/data` path. This includes MongoDB files located in the `/mongodb` subfolder and files created by the application under the `/artifacts` path.

## Seeding

For convenience, a new user is created with seeded data. If you need to change the templates, modify the files in the `/data/seed` folder.

## Service Configuration

Service-to-service communication is defined in the `docker-compose.yaml` file and `docker.env`. Please change port allocations or service names as required.

## Use Cases

### [Getting Started](https://www.youtube.com/watch?v=AyOjDZKjO-E)

### [![Create Job Artifacts](https://img.youtube.com/vi/6FcLRjC9KP4/0.jpg)](https://www.youtube.com/watch?v=6FcLRjC9KP4)

### [Add Job Post Url Manually](https://youtu.be/6JPFdrpvM8Q)

### [Add a Note to a Rejected Application](https://youtu.be/4zPbxFxEpGM)

### [Refresh LinkedIn Profile Headline](https://youtu.be/nz_kqNzbV-w)
