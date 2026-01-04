# Contributing

Thanks for your interest in contributing.

Ways to contribute
- File issues for bugs, dataset problems, or feature requests.
- Open pull requests with clear scope and tests.
- Improve docs, add notebooks, or enhance reproducibility.

How to contribute
1. Fork the repository.
2. Create a branch: `git checkout -b feat/short-description`.
3. Make changes, add tests, run `pytest` and notebook checks.
4. Run linters: `pre-commit run --all-files`.
5. Submit a PR with a clear description and link to relevant issues.

Development environment
- Create an environment using `environment.yml` or `requirements.txt`.
- Use `pre-commit` for formatting and checks.

Notebooks
- Keep notebooks small, focused, and reproducible.
- Put heavy processing code into `src/` and import it in notebooks.
- Add a short markdown summary at the top: goal, inputs, outputs, runtime.

Testing and CI
- All code should have unit tests where reasonable.
- Notebooks should run end-to-end in CI (nbval or papermill).

Code of conduct
- This project follows the Contributor Covenant. See CODE_OF_CONDUCT.md.

License
- Code: `LICENSE` file (MIT).
- Data: `LICENSE-DATA` (CC BY 4.0). See those files for details.

Contact
- Repository owner: @DulithMH
