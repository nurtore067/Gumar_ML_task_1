# Gumar — ML Task 1

MOP 3231 · Week 2 · Data Preprocessing and Cleaning  
Student-ID seed: **3242**

## Files

- `task1_preprocessing.ipynb`: executed notebook, with tables, explanations and plots.
- `requirements.txt`: the four exact package versions required by the assignment.
- `data/almaty_apartments_raw.csv`: original input.
- `data/almaty_apartments_clean.csv`: cleaned data with missing values still unfilled.

The supplied ZIP includes the real Git history. Extract the entire project folder,
including `.git`; do not copy only the visible notebook to a different repository.
The included commits were created by the automated assistant during preparation.

## Results for seed 3242

- Sample: 1,154 rows representing 1,080 listing IDs.
- Removed 33 exact duplicate rows and resolved 41 reposts by latest date.
- Corrected 11 supported factor-of-ten area errors; kept one plausible price outlier.
- Train/test matrices: 864 × 17 and 216 × 17, with no missing values.
- Test R²: 0.910490, used only as a preprocessing sanity check.

The prices are synthetic and do not describe the real Almaty property market.

## Быстро отправить работу

1. Полностью распакуй ZIP. Открой папку `Gumar_ML_task_1` в VS Code.
2. На GitHub создай **пустой публичный** репозиторий `Gumar_ML_task_1`.
   Не добавляй README, `.gitignore` или лицензию при создании.
3. В терминале VS Code, находясь в распакованной папке проекта, выполни команды
   ниже. Замени `YOUR_USERNAME` своим логином GitHub:

```powershell
git log --oneline
git remote add origin https://github.com/YOUR_USERNAME/Gumar_ML_task_1.git
git push -u origin main
git rev-parse HEAD
```

4. Открой загруженный notebook на GitHub: проверь, что видны результаты и графики.
5. Скопируй хеш из последней команды и сдай в Canvas ссылку:
   `https://github.com/YOUR_USERNAME/Gumar_ML_task_1/commit/HASH`

Нужна именно ссылка на **финальный commit**. Дедлайн из задания:
27 сентября 2026, 23:59 (UTC+5). Поздние коммиты не оцениваются.
Если репозиторий приватный, преподавателю `unreal-kz` необходимо дать доступ до дедлайна.

## Local environment and reproducibility

The notebook was executed from its first code cell through its last with Python
3.12.14, NumPy 2.0.2, pandas 2.3.3, matplotlib 3.9.4 and scikit-learn 1.6.1.
All notebook code cells completed successfully. Outputs were captured using an
in-process IPython session because the execution host disallows Jupyter socket
binding. A desktop VS Code Restart & Run All remains the local check for the
student's own kernel setup.

For the assignment's isolated environment, use Python 3.12. On Windows:

```powershell
py -3.12 -m venv .Gumar_ML_task_1
Set-ExecutionPolicy -Scope Process -ExecutionPolicy Bypass
.\.Gumar_ML_task_1\Scripts\Activate.ps1
python -m pip install -r requirements.txt
python -m pip install ipykernel
```

On macOS/Linux:

```bash
python3.12 -m venv .Gumar_ML_task_1
source .Gumar_ML_task_1/bin/activate
python -m pip install -r requirements.txt
python -m pip install ipykernel
```

Select this environment as the notebook kernel and use Restart & Run All.
Jupyter/ipykernel is a notebook tool and is intentionally not listed among the
four code dependencies in `requirements.txt`. The environment directory is ignored
by Git and is not included in the ZIP.

After rerunning or editing, commit and push the updated outputs, then submit the
new final commit URL:

```powershell
git add task1_preprocessing.ipynb data/almaty_apartments_clean.csv
git commit -m "Verify notebook in local project environment"
git push
git rev-parse HEAD
```
