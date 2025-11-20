## 🚀 Installation

Create a new virtual environment for Python. This can be skipped if you already have a working venv.

```sh
python -m venv venv
```

Activate the venv and install or update dependencies.

```sh
source venv/bin/activate \\
pip install -r requirements.txt
```

## 💡 Usage

Serve the documentation locally for live preview while developing:

```sh
zensical serve
```

This will run a local web server with the documentation accessible at <http://localhost:8000/>.

You can also build the website files directly:

```sh
zensical build
```

The output will be saved to `site/`.
